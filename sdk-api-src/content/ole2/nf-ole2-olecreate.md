---
UID: NF:ole2.OleCreate
title: OleCreate function
author: windows-sdk-content
description: Creates an embedded object identified by a CLSID. You use it typically to implement the menu item that allows the end user to insert a new object.
old-location: com\olecreate.htm
old-project: com
ms.assetid: 00b7edd2-8e2e-4e0a-91a6-d966f6c8d456
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: OleCreate, OleCreate function [COM], _ole_OleCreate, com.olecreate, ole/OleCreate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: ole2.h
req.include-header: Ole2.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: QACONTROL
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
api_name:
 - OleCreate
product: Windows
targetos: Windows
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
req.product: ADAM
---

# OleCreate function


## -description


Creates an embedded object identified by a CLSID. You use it typically to implement the menu item that allows the end user to insert a new object.




## -parameters




#### - rclsid [in]

CLSID of the embedded object that is to be created.


#### - riid [in]

Reference to the identifier of the interface, usually IID_IOleObject (defined in the OLE headers as the interface identifier for <a href="https://msdn.microsoft.com/58b32c87-39b6-4d64-9174-cf798ed302c2">IOleObject</a>), through which the caller will communicate with the new object.


#### - renderopt [in]

A value from the enumeration <a href="https://msdn.microsoft.com/bab871ba-4ec4-49fd-854a-585732b91290">OLERENDER</a>, indicating the locally cached drawing capabilities the newly created object is to have. The <b>OLERENDER</b> value chosen affects the possible values for the <i>pFormatEtc</i> parameter.


#### - pFormatEtc [in]

Depending on which of the <a href="https://msdn.microsoft.com/bab871ba-4ec4-49fd-854a-585732b91290">OLERENDER</a> flags is used as the value of renderopt, pointer to one of the <a href="https://msdn.microsoft.com/4478eb9a-84a1-4f3a-8290-94b8dd20c081">FORMATETC</a> enumeration values. Refer to the <b>OLERENDER</b> enumeration for restrictions. This parameter, along with the <i>renderopt</i> parameter, specifies what the new object can cache initially.


#### - pClientSite [in]

If you want <b>OleCreate</b> to call <a href="https://msdn.microsoft.com/6690b5a3-bada-496c-89cb-a9ae1fc9dfb0">IOleObject::SetClientSite</a>, pointer to the <a href="https://msdn.microsoft.com/dafee149-926a-4d08-a43d-5847682db645">IOleClientSite</a> interface on the container. The value may be <b>NULL</b>, in which case you must specifically call <b>IOleObject::SetClientSite</b> before attempting operations.


#### - pStg [in]

Pointer to an instance of the <a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a> interface on the storage object. This parameter may not be <b>NULL</b>.


#### - ppvObj [out]

Address of pointer variable that receives the interface pointer requested in riid. Upon successful return, *<i>ppvObject</i> contains the requested interface pointer.


## -returns



This function returns S_OK on success and supports the standard return value E_OUTOFMEMORY.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory for the operation.

</td>
</tr>
</table>
 




## -remarks



The <b>OleCreate</b> function creates a new embedded object, and is typically called to implement the menu item Insert New Object. When <b>OleCreate</b> returns, the object it has created is blank (contains no data), unless <i>renderopt</i> is OLERENDER_DRAW or OLERENDER_FORMAT, and is loaded. Containers typically then call the <a href="https://msdn.microsoft.com/9035f996-b163-4855-aa9d-184b77072ead">OleRun</a> function or <a href="https://msdn.microsoft.com/fabd6a0a-7b0c-4c99-af22-8b117addd5f7">IOleObject::DoVerb</a> to show the object for initial editing.



The <i>rclsid</i> parameter specifies the CLSID of the requested object. CLSIDs of registered objects are stored in the system registry. When an application user selects Insert Object, a selection box allows the user to select the type of object desired from those in the registry. When <b>OleCreate</b> is used to implement the Insert Object menu item, the CLSID associated with the selected item is assigned to the rclsid parameter of <b>OleCreate</b>.



The <i>riid</i> parameter specifies the interface the client will use to communicate with the new object. Upon successful return, the <i>ppvObject</i> parameter holds a pointer to the requested interface.



The created object's cache contains information that allows a presentation of a contained object when the container is opened. Information about what should be cached is passed in the <i>renderopt</i> and <i>pFormatetc</i> values. When <b>OleCreate</b> returns, the created object's cache is not necessarily filled. Instead, the cache is filled the first time the object enters the running state. The caller can add additional cache control with a call to <a href="https://msdn.microsoft.com/2a86063a-3ee6-4fc2-a6e0-6e9ffa658348">IOleCache::Cache</a> after the return of <b>OleCreate</b> and before the object is run. If renderopt is OLERENDER_DRAW or OLERENDER_FORMAT, <b>OleCreate</b> requires that the object support the <a href="https://msdn.microsoft.com/b5ef85d0-b54e-4831-87f1-ac6763179181">IOleCache</a> interface. There is no such requirement for any other value of renderopt.

If <i>pClientSite</i> is non-<b>NULL</b>, <b>OleCreate</b> calls <a href="https://msdn.microsoft.com/6690b5a3-bada-496c-89cb-a9ae1fc9dfb0">IOleObject::SetClientSite</a> through the <i>pClientSite</i> pointer. <a href="https://msdn.microsoft.com/dafee149-926a-4d08-a43d-5847682db645">IOleClientSite</a> is the primary interface by which an object requests services from its container. If <i>pClientSite</i> is <b>NULL</b>, you must make a specific call to <b>IOleObject::SetClientSite</b> before attempting any operations. 





## -see-also




<a href="https://msdn.microsoft.com/4478eb9a-84a1-4f3a-8290-94b8dd20c081">FORMATETC</a>



<a href="https://msdn.microsoft.com/dafee149-926a-4d08-a43d-5847682db645">IOleClientSite</a>



<a href="https://msdn.microsoft.com/58b32c87-39b6-4d64-9174-cf798ed302c2">IOleObject</a>



<a href="https://msdn.microsoft.com/bab871ba-4ec4-49fd-854a-585732b91290">OLERENDER</a>
 

 

