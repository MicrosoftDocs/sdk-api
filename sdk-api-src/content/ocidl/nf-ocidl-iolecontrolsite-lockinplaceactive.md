---
UID: NF:ocidl.IOleControlSite.LockInPlaceActive
title: IOleControlSite::LockInPlaceActive (ocidl.h)
author: windows-sdk-content
description: Indicates whether a control should remain in-place active. Calls to this method typically nest an event to ensure that the object's activation state remains stable throughout the processing of the event.
old-location: com\iolecontrolsite_lockinplaceactive.htm
tech.root: com
ms.assetid: abd9a6c6-1551-4423-b1d6-f735159f6df4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IOleControlSite interface [COM],LockInPlaceActive method, IOleControlSite.LockInPlaceActive, IOleControlSite::LockInPlaceActive, LockInPlaceActive, LockInPlaceActive method [COM], LockInPlaceActive method [COM],IOleControlSite interface, _ctrl_iolecontrolsite_lockinplaceactive, com.iolecontrolsite_lockinplaceactive, ocidl/IOleControlSite::LockInPlaceActive
ms.topic: method
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - IOleControlSite.LockInPlaceActive
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOleControlSite::LockInPlaceActive


## -description


Indicates whether a control should remain in-place active. Calls to this method typically nest an event to ensure that the object's activation state remains stable throughout the processing of the event.


## -parameters




### -param fLock [in]

Indicates whether to ensure the in-place active state (<b>TRUE</b>) or to allow activation to change (<b>FALSE</b>). When <b>TRUE</b>, a supporting container must not deactivate the in-place object until this method is called again with <b>FALSE</b>.


## -returns



This method can return the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The lock or unlock was made successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The container does not support in-place locking.

</td>
</tr>
</table>
 




## -remarks



This method affects the control's in-place active state but not its UI-active state.




## -see-also




<a href="https://msdn.microsoft.com/8b022f2c-d4b4-44ca-8e69-46e9aa20b3f9">IOleControlSite</a>
 

 

