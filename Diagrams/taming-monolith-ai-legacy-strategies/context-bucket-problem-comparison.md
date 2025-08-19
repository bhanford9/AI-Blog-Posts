# Context Bucket Problem: Greenfield vs Monolith

## Visual Metaphor Diagram

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                          AI CONTEXT CAPACITY COMPARISON                     │
└─────────────────────────────────────────────────────────────────────────────┘

GREENFIELD PROJECT                          MONOLITHIC CODEBASE
┌─────────────────────┐                    ┌─────────────────────┐
│    Clean Bucket     │                    │   Overflowing       │
│                     │                    │     Bucket          │
│  ┌─────────────┐    │                    │                     │
│  │ Current     │    │                    │  ┌─────┐ ┌─────┐    │
│  │ Feature     │    │                    │  │Code │ │Config│    │
│  │ Code        │    │                    │  └─────┘ └─────┘    │
│  └─────────────┘    │                    │  ┌─────┐ ┌─────┐    │
│                     │                    │  │Build│ │Tests│    │
│  ┌─────────────┐    │                    │  └─────┘ └─────┘    │
│  │ Related     │    │                    │  ┌─────┐ ┌─────┐    │
│  │ Utils       │    │                    │  │Deps │ │Hist │    │ ⮞ OVERFLOW
│  └─────────────┘    │                    │  └─────┘ └─────┘    │
│                     │                    │     ⮟  ⮟  ⮟        │
│  Available Space    │                    │  Lost Context       │
│                     │                    │                     │
└─────────────────────┘                    └─────────────────────┘

✅ MANAGEABLE CONTEXT                      ❌ CONTEXT OVERLOAD
- All code fits in bucket                 - Too much information
- Clear understanding possible            - Must discard knowledge
- AI can see full picture                 - Partial understanding only
- Effective reasoning                     - Degraded performance

THE IMPOSSIBLE CHOICE
┌─────────────────────────────────────────────────────────────────┐
│  When new information arrives in monolithic environment:        │
│                                                                 │
│  New Code    ┌─ Keep existing knowledge → Reject new info      │
│     ⮟        │                                                 │
│  Full Bucket ┴─ Accept new info → Discard existing knowledge   │
│                                                                 │
│  Either choice results in incomplete understanding!            │
└─────────────────────────────────────────────────────────────────┘
```

## Visual Requirements
- **Use clear see-through buckets to show elements within them**
- **Show that the full bucket cannot fit the next item**
- **Show that the bucket with room can fit the next item**

## Key Concepts

### Greenfield Advantages
- **Limited Scope**: Only current work and immediate dependencies
- **Clean Context**: All information is relevant and related
- **Full Understanding**: AI can comprehend entire relevant codebase
- **Optimal Performance**: AI operates within natural capacity limits

### Monolithic Challenges
- **Information Overload**: Vast amounts of interconnected code
- **Context Fragmentation**: Must choose what to remember/forget
- **Partial Understanding**: Never has complete picture
- **Performance Degradation**: Struggles with complex reasoning

### The Context Bucket Metaphor
The AI's working memory is like a fixed-size bucket:
- **Greenfield**: Bucket contains only what you need
- **Monolith**: Bucket overflows, forcing difficult trade-offs
- **Key Insight**: Success requires working within bucket limitations

## Implementation Notes
This diagram should be placed after the "Context Bucket Problem" section to visually reinforce the core metaphor that underlies all subsequent strategies in the article.
