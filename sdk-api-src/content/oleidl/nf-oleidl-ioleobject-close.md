---
UID: NF:oleidl.IOleObject.Close
title: IOleObject::Close
author: windows-sdk-content
description: Changes an embedded object from the running to the loaded state. Disconnects a linked object from its link source.
old-location: com\ioleobject_close.htm
old-project: com
ms.assetid: 61ecd153-ed6b-4a2c-a862-54742c5769ee
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: Close, Close method [COM], Close method [COM],IOleObject interface, IOleObject interface [COM],Close method, IOleObject.Close, IOleObject::Close, _ole_ioleobject_close, com.ioleobject_close, oleidl/IOleObject::Close
ms.prod: windows
ms.technology: windows-sdk
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
-	IOleObject.Close
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IOleObject::Close


## -description


Changes an embedded object from the running to the loaded state. Disconnects a linked object from its link source.


## -parameters




### -param dwSaveOption [in]

Indicates whether the object is to be saved as part of the transition to the loaded state. Valid values are taken from the enumeration <a href="https://msdn.microsoft.com/386f24a4-11d7-4471-960e-1a3ff67ba3c5">OLECLOSE</a>.

<div class="alert"><b>Note</b>  The OLE 2 user model recommends that object applications do not prompt users before saving linked or embedded objects, including those activated in place. This policy represents a change from the OLE 1 user model, in which object applications always prompt the user to decide whether to save changes.</div>
<div> </div>

## -returns



This method returns S_OK on success. Other possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_E_PROMPTSAVECANCELLED</b></dt>
</dl>
</td>
<td width="60%">
The user was prompted to save but chose the <b>Cancel</b> button from the prompt message box.

</td>
</tr>
</table>
 




## -remarks



<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
A container application calls <b>IOleObject::Close</b> when it wants to move the object from a running to a loaded state. Following such a call, the object still appears in its container but is not open for editing. Calling <b>IOleObject::Close</b> on an object that is loaded but not running has no effect. Closing a linked object simply means disconnecting it.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
Upon receiving a call to <b>IOleObject::Close</b>, a running object should do the following:

<ul>
<li>If the object has been changed since it was last opened for editing, it should request to be saved, or not, according to instructions specified in <i>dwSaveOption</i>. If the option is to save the object, then it should call its container's <a href="https://msdn.microsoft.com/ef1a0085-f4fa-4d77-adab-0386f354dfe7">IOleClientSite::SaveObject</a> interface.</li>
<li>If the object has <a href="https://msdn.microsoft.com/be9891d4-aad3-42a0-8c8e-4b86091ff03b">IDataObject::DAdvise</a> connections with <a href="https://msdn.microsoft.com/e1ad9c17-e492-4891-bf1d-cbac48ce537a">ADVF</a>_DATAONSTOP flags, then it should send an <a href="https://msdn.microsoft.com/834a5328-3a1f-4edb-aad0-be8ab87acb04">IAdviseSink::OnDataChange</a> notification. See <b>IDataObject::DAdvise</b> for details.</li>
<li>If the object currently owns the Clipboard, it should empty it by calling <a href="https://msdn.microsoft.com/18291a91-be7d-42ec-a44a-d1bbfb017c6e">OleFlushClipboard</a>.</li>
<li>If the object is currently visible, notify its container by calling <a href="https://msdn.microsoft.com/9185add8-02d1-4bf3-99ff-82f64ba12ef4">IOleClientSite::OnShowWindow</a> with the <i>fshow</i> argument set to <b>FALSE</b>.</li>
<li>Send <a href="https://msdn.microsoft.com/a695c623-4a4e-4f3d-9f12-ee198c0761a9">IAdviseSink::OnClose</a> notifications to appropriate advise sinks.</li>
<li>Finally, forcibly cut off all remoting clients by calling <a href="https://msdn.microsoft.com/4293316a-bafe-4fca-ad6a-68d8e99c8fba">CoDisconnectObject</a>.</li>
</ul>
If the object application is a local server (an EXE rather than a DLL), closing the object should also shut down the object application unless the latter is supporting other running objects or has another reason to remain in the running state. Such reasons might include the presence of <a href="https://msdn.microsoft.com/4c817b89-013d-477f-a713-5e320896dfa0">IClassFactory::LockServer</a> locks, end-user control of the application, or the existence of other open documents requiring access to the application.

Calling <b>IOleObject::Close</b> on a linked object disconnects it from, but does not shut down, its source application. A source application that is visible to the user when the object is closed remains visible and running after the disconnection and does not send an <a href="https://msdn.microsoft.com/a695c623-4a4e-4f3d-9f12-ee198c0761a9">IAdviseSink::OnClose</a> notification to the link container.




## -see-also




<a href="https://msdn.microsoft.com/4293316a-bafe-4fca-ad6a-68d8e99c8fba">CoDisconnectObject</a>



<a href="https://msdn.microsoft.com/a695c623-4a4e-4f3d-9f12-ee198c0761a9">IAdviseSink::OnClose</a>



<a href="https://msdn.microsoft.com/4c817b89-013d-477f-a713-5e320896dfa0">IClassFactory::LockServer</a>



<a href="https://msdn.microsoft.com/be9891d4-aad3-42a0-8c8e-4b86091ff03b">IDataObject::DAdvise</a>



<a href="https://msdn.microsoft.com/9185add8-02d1-4bf3-99ff-82f64ba12ef4">IOleClientSite::OnShowWindow</a>



<a href="https://msdn.microsoft.com/ef1a0085-f4fa-4d77-adab-0386f354dfe7">IOleClientSite::SaveObject</a>



<a href="https://msdn.microsoft.com/58b32c87-39b6-4d64-9174-cf798ed302c2">IOleObject</a>



<a href="https://msdn.microsoft.com/386f24a4-11d7-4471-960e-1a3ff67ba3c5">OLECLOSE</a>



<a href="https://msdn.microsoft.com/18291a91-be7d-42ec-a44a-d1bbfb017c6e">OleFlushClipboard</a>
 

 

