---
UID: NF:oleidl.IOleAdviseHolder.SendOnSave
title: IOleAdviseHolder::SendOnSave method
author: windows-driver-content
description: Sends notification to all advisory sinks currently registered with the advise holder that the object has been saved.
old-location: com\ioleadviseholder_sendonsave.htm
old-project: com
ms.assetid: b64ceaf7-45ba-4a66-a5cf-aec352472d3d
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: IOleAdviseHolder, IOleAdviseHolder interface [COM], SendOnSave method, IOleAdviseHolder::SendOnSave, SendOnSave method [COM], SendOnSave method [COM], IOleAdviseHolder interface, SendOnSave,IOleAdviseHolder.SendOnSave, _ole_ioleadviseholder_sendonsave, com.ioleadviseholder_sendonsave, oleidl/IOleAdviseHolder::SendOnSave
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OleIdl.Idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: USERCLASSTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	OleIdl.h
api_name:
-	IOleAdviseHolder.SendOnSave
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IOleAdviseHolder::SendOnSave method


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
 

 

