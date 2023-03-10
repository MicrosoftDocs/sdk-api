---
UID: NN:faxcomex.IFaxServerNotify2
title: IFaxServerNotify2 (faxcomex.h)
description: The IFaxServerNotify2 interface is used for fax notifications. (IIFaxServerNotify2)
helpviewer_keywords: ["IFaxServerNotify2","IFaxServerNotify2 interface [Fax Service]","IFaxServerNotify2 interface [Fax Service]","described","IIFaxServerNotify2","_mfax_ifaxservernotify2","fax._mfax_ifaxservernotify2","faxcomex/IFaxServerNotify2"]
old-location: fax\_mfax_ifaxservernotify2.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxservernotify2\faxinto_z_ifaxservernotify2.htm
ms.date: 12/05/2018
ms.keywords: IFaxServerNotify2, IFaxServerNotify2 interface [Fax Service], IFaxServerNotify2 interface [Fax Service],described, IIFaxServerNotify2, _mfax_ifaxservernotify2, fax._mfax_ifaxservernotify2, faxcomex/IFaxServerNotify2
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
 - IFaxServerNotify2
 - faxcomex/IFaxServerNotify2
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
 - IFaxServerNotify2
 - IIFaxServerNotify2
---

# IFaxServerNotify2 interface


## -description

The <b>IFaxServerNotify2</b> interface is used for fax notifications. The fax service calls <b>IFaxServerNotify2</b> to send fax event notifications. Events include changes to fax server configuration and activity, changes to incoming and outgoing job queues, and changes to incoming and outgoing archives. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-registering-for-event-notifications">Registering for Event Notifications</a>.

The <b>IFaxServerNotify2</b> interface supports all the same methods as the <a href="/windows/desktop/api/faxcomex/nn-faxcomex-ifaxservernotify2">IFaxServerNotify</a> interface and the additional method <a href="/windows/win32/api/faxcomex/nf-faxcomex-_ifaxservernotify2-ongeneralserverconfigchanged">OnGeneralServerConfigChanged</a>.

## -inheritance

The <b>IFaxServerNotify2</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFaxServerNotify2</b> also has these types of members:

## -remarks

<h3><a id="To_Use_Fax_Notification_Events_with_Visual_Basic"></a><a id="to_use_fax_notification_events_with_visual_basic"></a><a id="TO_USE_FAX_NOTIFICATION_EVENTS_WITH_VISUAL_BASIC"></a>To Use Fax Notification Events with Visual Basic</h3>
Use the following syntax when creating the root FaxServer2 object:



```

Dim WithEvents objFaxServer2 As FaxServer2

```




For an example, see <a href="/previous-versions/windows/desktop/fax/-mfax-registering-for-fax-events">Registering for Fax Events</a>.
            

<h3><a id="To_Use_Fax_Notification_Events_with_C__"></a><a id="to_use_fax_notification_events_with_c__"></a><a id="TO_USE_FAX_NOTIFICATION_EVENTS_WITH_C__"></a>To Use Fax Notification Events with C++</h3>
A fax client application must implement <b>IFaxServerNotify2</b> and pass the fax service the pointer to an <b>IFaxServerNotify2</b> interface.
