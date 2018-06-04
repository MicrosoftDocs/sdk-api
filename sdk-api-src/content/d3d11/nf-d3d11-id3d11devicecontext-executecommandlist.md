---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# ID3D11DeviceContext::ExecuteCommandList


## -description


Queues commands from a command list onto a device.


## -parameters




### -param pCommandList [in]

Type: <b><a href="https://msdn.microsoft.com/432f1d21-bf13-4569-9c8f-04f5d2845150">ID3D11CommandList</a>*</b>


            A pointer to an <a href="https://msdn.microsoft.com/432f1d21-bf13-4569-9c8f-04f5d2845150">ID3D11CommandList</a> interface that encapsulates a command list.
          


### -param RestoreContextState

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>


            A Boolean flag that determines whether the target context state is saved prior to and restored after the execution of a command list. Use <b>TRUE</b> to indicate that the runtime needs to save and restore the state. Use <b>FALSE</b> to indicate that no state shall be saved or restored, which causes the target context to  return to its default state after the command list executes. Applications should typically use <b>FALSE</b> unless they will restore the state to be nearly equivalent to the state that the runtime would restore if <b>TRUE</b> were passed. When applications use <b>FALSE</b>, they can avoid unnecessary and inefficient state transitions.
          


## -returns



This method does not return a value.




## -remarks



Use this method to play back a command list that was recorded by a deferred context on any thread.


          A call to <b>ExecuteCommandList</b> of a command list from a deferred context onto the immediate context is required for the recorded commands to be executed on the graphics processing unit (GPU). A call to <b>ExecuteCommandList</b> of a command list from a deferred context onto another deferred context can be used to merge recorded lists. But to run the commands from the merged deferred command list on the GPU, you need to execute them on the immediate context.
        


          This method performs some runtime validation related to queries. Queries that are begun in a device context cannot be manipulated indirectly by executing a command list (that is, Begin or End was invoked against the same query by the deferred context which generated the command list). If such a condition occurs, the ExecuteCommandList method does not execute the command list. However, the state of the device context is still maintained, as would be expected (<a href="https://msdn.microsoft.com/dabf52f5-0f69-4017-863c-9e3ecef4d5dc">ID3D11DeviceContext::ClearState</a> is performed, unless the application indicates to preserve the device context state).
        

<b>Windows Phone 8:
        </b> This API is supported.
      




## -see-also




<a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a>
 

 

