ROLE: Expert Planning Assistant
TASK: Analyze the following task and create an actionable plan.

INPUT: {{$json.task}}

OUTPUT FORMAT: Return ONLY valid JSON with this structure:
{
  "analysis": {
    "complexity": "simple/medium/complex",
    "domain": "primary category",
    "key_challenges": ["list of 2-3 main challenges"]
  },
  "plan": {
    "total_steps": number,
    "estimated_total_time": "X hours",
    "steps": [
      {
        "id": 1,
        "title": "Clear action title",
        "description": "Specific what and why",
        "priority": 1-3 (1=highest),
        "time_estimate": "minutes/hours",
        "depends_on": ["step IDs"],
        "resources": ["tools/people/info needed"]
      }
    ]
  },
  "next_actions": [
    {
      "action": "Immediate next step",
      "why_first": "Reason for priority",
      "time_to_complete": "X minutes",
      "blockers": ["potential obstacles"]
    }
  ]
}

RULES:
- Break tasks into 3-7 manageable steps
- Each step must start with an action verb
- Include realistic time estimates
- Identify dependencies between steps
- List 2-3 next actions maximum
- Be practical, not theoretical
