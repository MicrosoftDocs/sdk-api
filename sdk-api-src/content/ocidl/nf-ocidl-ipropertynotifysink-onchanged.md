---
UID: NF:ocidl.IPropertyNotifySink.OnChanged
title: IPropertyNotifySink::OnChanged
author: windows-sdk-content
description: Notifies a sink that a bindable property has changed.
old-location: com\ipropertynotifysink_onchanged.htm
old-project: com
ms.assetid: 71ab5206-5127-45f1-a2b5-3fbcc867d678
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: IPropertyNotifySink interface [COM],OnChanged method, IPropertyNotifySink.OnChanged, IPropertyNotifySink::OnChanged, OnChanged, OnChanged method [COM], OnChanged method [COM],IPropertyNotifySink interface, _ctrl_ipropertynotifysink_onchanged, com.ipropertynotifysink_onchanged, ocidl/IPropertyNotifySink::OnChanged
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: VIEWSTATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - IPropertyNotifySink.OnChanged
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IPropertyNotifySink::OnChanged


## -description


Notifies a sink that a <a href="https://msdn.microsoft.com/ba09096d-a2f7-4958-827c-0fba19ded26f">bindable</a> property has changed.


## -parameters




### -param dispID [in]

The dispatch identifier of the property that changed, or DISPID_UNKNOWN if multiple properties have changed. The client (owner of the sink) should retrieve the current value of each property of interest from the object that generated the notification.


## -returns



This method returns S_OK in all cases.




## -remarks



S_OK is returned in all cases even when the sink does not need [<a href="https://msdn.microsoft.com/ba09096d-a2f7-4958-827c-0fba19ded26f">bindable</a>] properties or when some other failure has occurred. In short, the calling object simply sends the notification and cannot attempt to use an error code (such as E_NOTIMPL) to determine whether to not send the notification in the future. Such semantics are not part of this interface.




## -see-also




<a href="https://msdn.microsoft.com/bfdf315c-6375-4c77-abd8-03f07342820f">IPropertyNotifySink</a>
 

 

