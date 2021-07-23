---
UID: NN:adhoc.IDot11AdHocManagerNotificationSink
title: IDot11AdHocManagerNotificationSink (adhoc.h)
description: Defines the notifications supported by the IDot11AdHocManager interface.
helpviewer_keywords: ["IDot11AdHocManagerNotificationSink","IDot11AdHocManagerNotificationSink interface [NativeWIFI]","IDot11AdHocManagerNotificationSink interface [NativeWIFI]","described","adhoc/IDot11AdHocManagerNotificationSink","nwifi.idot11adhocmanagernotificationsink"]
old-location: nwifi\idot11adhocmanagernotificationsink.htm
tech.root: nwifi
ms.assetid: a79931ad-deeb-4e46-a051-80a57fe5935c
ms.date: 12/05/2018
ms.keywords: IDot11AdHocManagerNotificationSink, IDot11AdHocManagerNotificationSink interface [NativeWIFI], IDot11AdHocManagerNotificationSink interface [NativeWIFI],described, adhoc/IDot11AdHocManagerNotificationSink, nwifi.idot11adhocmanagernotificationsink
req.header: adhoc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Adhoc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDot11AdHocManagerNotificationSink
 - adhoc/IDot11AdHocManagerNotificationSink
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - adhoc.h
api_name:
 - IDot11AdHocManagerNotificationSink
---

# IDot11AdHocManagerNotificationSink interface


## -description

The <b>IDot11AdHocManagerNotificationSink</b> interface defines the notifications supported by the <a href="/windows/desktop/api/adhoc/nn-adhoc-idot11adhocmanager">IDot11AdHocManager</a> interface. To register for notifications, call the  <a href="/windows/desktop/api/ocidl/nf-ocidl-iconnectionpoint-advise">Advise</a> method on an instantiated <a href="/windows/desktop/api/adhoc/nn-adhoc-idot11adhocmanager">IDot11AdHocManager</a> object with the <b>IDot11AdHocManagerNotificationSink</b> interface passed  as the <i>pUnk</i>  parameter.  To terminate notifications, call the <a href="/windows/desktop/api/ocidl/nf-ocidl-iconnectionpoint-unadvise">Unadvise</a> method.
<div class="alert"><b>Note</b>  Ad hoc mode might not be available in future versions of Windows. Starting with Windows 8.1 and Windows Server 2012 R2, use <a href="/windows/desktop/NativeWiFi/about-the-wi-fi-direct-api">Wi-Fi Direct</a> instead.</div><div> </div>

## -inheritance

The <b>IDot11AdHocManagerNotificationSink</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDot11AdHocManagerNotificationSink</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/adhoc/nn-adhoc-idot11adhocmanager">IDot11AdHocManager</a>
