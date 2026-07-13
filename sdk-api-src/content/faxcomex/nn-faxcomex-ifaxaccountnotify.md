---
UID: NN:faxcomex.IFaxAccountNotify
title: IFaxAccountNotify (faxcomex.h)
description: Called by the fax service to send event notifications about particular fax accounts. This property sends event notifications. Events include changes to incoming and outgoing job queues, and changes to incoming and outgoing archives. (IIFaxAccountNotify)
helpviewer_keywords: ["IFaxAccountNotify","IFaxAccountNotify interface [Fax Service]","IFaxAccountNotify interface [Fax Service]","described","IIFaxAccountNotify","_IFaxAccountNotify","_mfax_ifaxaccountnotify","fax._mfax_ifaxaccountnotify","faxcomex/_IFaxAccountNotify"]
old-location: fax\_mfax_ifaxaccountnotify.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxaccountnotify\faxinto_z_ifaxaccountnotify.htm
ms.date: 12/05/2018
ms.keywords: IFaxAccountNotify, IFaxAccountNotify interface [Fax Service], IFaxAccountNotify interface [Fax Service],described, IIFaxAccountNotify, _IFaxAccountNotify, _mfax_ifaxaccountnotify, fax._mfax_ifaxaccountnotify, faxcomex/_IFaxAccountNotify
req.header: faxcomex.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFaxAccountNotify
 - faxcomex/IFaxAccountNotify
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - IFaxAccountNotify
 - IIFaxAccountNotify
---

# IFaxAccountNotify interface


## -description

Called by the fax service to send event notifications about particular fax accounts. This property sends event notifications. Events include changes to incoming and outgoing job queues, and changes to incoming and outgoing archives.

## -inheritance

The <b>IFaxAccountNotify</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>_IFaxAccountNotify</b> also has these types of members:

## -remarks

<h3><a id="To_Use_Fax_Notification_Events_with_Visual_Basic"></a><a id="to_use_fax_notification_events_with_visual_basic"></a><a id="TO_USE_FAX_NOTIFICATION_EVENTS_WITH_VISUAL_BASIC"></a>To Use Fax Notification Events with Visual Basic</h3>
Use the following syntax when creating the <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxaccount">IFaxAccount</a> object:



```

Dim WithEvents objFaxAccount As FaxAccount

```


<h3><a id="To_Use_Fax_Notification_Events_with_C__"></a><a id="to_use_fax_notification_events_with_c__"></a><a id="TO_USE_FAX_NOTIFICATION_EVENTS_WITH_C__"></a>To Use Fax Notification Events with C++</h3>
A fax client application must implement <b>IFaxAccountNotify</b> and pass the fax service the pointer to an <b>IFaxAccountNotify</b> interface.
