Mini-level — Inleveren
Naam: Timo van es
Klas: Datum:
Les: GDV Les 6

Wat heb ik gemaakt?
een versie van blik gooien

Screenshot / GIF van je level
Mini-level preview
![mini level]( src=""https://giphy.com/gifs/5DFLijf6IYAH0vrWuQ">)

Bewegend object:
Mijn bewegende object is een capsule die ik heb gekozen om te gebruiken als pittenzak in dit level.
using UnityEngine;

public class Pittenzak : MonoBehaviour
{
    [SerializeField] private float moveSpeed;
    [SerializeField] private Rigidbody rb;
    private Vector3 moveVector;

    private void Update()
    {
        CheckPlayerMovement();
    }

    private void CheckPlayerMovement()
    {
        moveVector.x = Input.GetAxis("Horizontal");
        moveVector.z = Input.GetAxis("Vertical");

        rb.linearVelocity = moveVector * moveSpeed;
    }

// Plak hier de OnCollisionEnter/OnTriggerEnter code die je hebt gebruikt.
private void OnTriggerEnter(Collider other)
{
using UnityEngine;
using UnityEngine.SceneManagement;

public class WinPlane : MonoBehaviour
{
    [Tooltip("The tag of the game object that triggers the win condition.")]
    [SerializeField] private string targetTag = "Player";

    private void OnTriggerEnter(Collider other)
    {
        if (other.CompareTag(targetTag))
        {
            Debug.Log("Level Won!");

            // Option A: Load the next level in the Build Settings
            int nextSceneIndex = SceneManager.GetActiveScene().buildIndex + 1;
            if (nextSceneIndex < SceneManager.sceneCountInBuildSettings)
            {
                SceneManager.LoadScene(nextSceneIndex);
            }
            else
            {
                // Fallback if this is the last level
                SceneManager.LoadScene("WinScreen");
 
public class CapsuleCollider : Collider
public class BoxCollider : Collider
public class BoxCollider : Collider
public class BoxCollider : Collider
public class BoxCollider : Collider
public class BoxCollider : Collider
public class BoxCollider : Collider
public class BoxCollider : Collider
public class BoxCollider : Collider
public class BoxCollider : Collider
public class BoxCollider : Collider

}
...

// Optioneel: plak hier de bijbehorende code.
Evaluatie
Wat ging goed? en waarom?
De code gebruiken want die had ik ook al in eerdere opdrachten gebruikt.

Wat vond je lastig? en waarom?
De camera deed steeds moeilijk want hij was aan het glitchen.
Wat zou je een volgende keer anders doen?
Minder grote objecten maken.
