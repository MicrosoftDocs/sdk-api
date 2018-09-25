---
UID: NF:ocidl.IOleControl.OnAmbientPropertyChange
title: IOleControl::OnAmbientPropertyChange
author: windows-sdk-content
description: Informs a control that one or more of the container's ambient properties has changed.
old-location: com\iolecontrol_onambientpropertychange.htm
tech.root: com
ms.assetid: 9ca43723-a14e-4f03-8eec-e10ab34ecb4d
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: IOleControl interface [COM],OnAmbientPropertyChange method, IOleControl.OnAmbientPropertyChange, IOleControl::OnAmbientPropertyChange, OnAmbientPropertyChange, OnAmbientPropertyChange method [COM], OnAmbientPropertyChange method [COM],IOleControl interface, _ctrl_iolecontrol_onambientpropertychange, com.iolecontrol_onambientpropertychange, ocidl/IOleControl::OnAmbientPropertyChange
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IOleControl.OnAmbientPropertyChange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOleControl::OnAmbientPropertyChange


## -description


Informs a control that one or more of the container's ambient properties has changed.


## -parameters




### -param dispID [in]

The dispatch identifier of the ambient property that changed. If this parameter is DISPID_UNKNOWN, it indicates that multiple properties changed. In this case, the control should check all the ambient properties of interest to obtain their current values.


## -returns



This method returns S_OK in all cases.




## -remarks



<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
S_OK is returned in all cases even when the control does not support ambient properties or some other failure has occurred. The caller sending the notification cannot attempt to use an error code (such as E_NOTIMPL) to determine whether to send the notification in the future. Such semantics are not part of this interface.




## -see-also




<a href="https://msdn.microsoft.com/ef85dce6-b680-4a72-9277-4cfdab27cbbc">IOleControl</a>
 

 

