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

# IOleAdviseHolder::SendOnSave


## -description


Sends notification to all advisory sinks currently registered with the advise holder that the object has been saved.


## -parameters






## -returns



This method returns S_OK if advise sinks were sent <a href="https://msdn.microsoft.com/26da5e16-5790-49c0-ba63-5feee49cd4c6">IAdviseSink::OnSave</a> notifications.




## -remarks



<b>SendOnSave</b> calls <a href="https://msdn.microsoft.com/26da5e16-5790-49c0-ba63-5feee49cd4c6">IAdviseSink::OnSave</a> to advise the calling object (client), which must have already established an advisory connection, that the object has been saved. If you are using the OLE advise holder (having obtained a pointer through a call to <a href="https://msdn.microsoft.com/f76e074e-6814-4735-9417-d5970e73089f">CreateOleAdviseHolder</a>), you can call <b>SendOnSave</b> whenever you save the object the advise holder is associated with.

To take the object from the running state to the loaded state, the client calls <a href="https://msdn.microsoft.com/61ecd153-ed6b-4a2c-a862-54742c5769ee">IOleObject::Close</a>. Within that implementation, if the user wants to save the object to persistent storage, the object calls <a href="https://msdn.microsoft.com/ef1a0085-f4fa-4d77-adab-0386f354dfe7">IOleClientSite::SaveObject</a>, followed by the call to <b>SendOnSave</b>.




## -see-also




<a href="https://msdn.microsoft.com/26da5e16-5790-49c0-ba63-5feee49cd4c6">IAdviseSink::OnSave</a>



<a href="https://msdn.microsoft.com/680afee7-2bee-4d54-ae0b-3e4e0deb622f">IOleAdviseHolder</a>
 

 

