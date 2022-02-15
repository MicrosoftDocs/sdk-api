---
UID: NN:adhoc.IDot11AdHocNetworkNotificationSink
title: IDot11AdHocNetworkNotificationSink (adhoc.h)
description: Defines the notifications supported by the IDot11AdHocNetwork interface.
helpviewer_keywords: ["IDot11AdHocNetworkNotificationSink","IDot11AdHocNetworkNotificationSink interface [NativeWIFI]","IDot11AdHocNetworkNotificationSink interface [NativeWIFI]","described","adhoc/IDot11AdHocNetworkNotificationSink","nwifi.idot11adhocnetworknotificationsink"]
old-location: nwifi\idot11adhocnetworknotificationsink.htm
tech.root: nwifi
ms.assetid: 54a45431-8036-4a3f-9558-467a1efab6bb
ms.date: 12/05/2018
ms.keywords: IDot11AdHocNetworkNotificationSink, IDot11AdHocNetworkNotificationSink interface [NativeWIFI], IDot11AdHocNetworkNotificationSink interface [NativeWIFI],described, adhoc/IDot11AdHocNetworkNotificationSink, nwifi.idot11adhocnetworknotificationsink
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
 - IDot11AdHocNetworkNotificationSink
 - adhoc/IDot11AdHocNetworkNotificationSink
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
 - IDot11AdHocNetworkNotificationSink
---

# IDot11AdHocNetworkNotificationSink interface


## -description

The <b>IDot11AdHocNetworkNotificationSink</b> interface defines the notifications supported by the <a href="/windows/desktop/api/adhoc/nn-adhoc-idot11adhocnetwork">IDot11AdHocNetwork</a> interface. To register for notifications, call the  <a href="/windows/desktop/api/ocidl/nf-ocidl-iconnectionpoint-advise">Advise</a> method on an instantiated <a href="/windows/desktop/api/adhoc/nn-adhoc-idot11adhocmanager">IDot11AdHocManager</a> object with the <b>IDot11AdHocNetworkNotificationSink</b> interface passed  as the <i>pUnk</i>  parameter.  To terminate notifications, call the <a href="/windows/desktop/api/ocidl/nf-ocidl-iconnectionpoint-unadvise">Unadvise</a> method.
<div class="alert"><b>Note</b>  Ad hoc mode might not be available in future versions of Windows. Starting with Windows 8.1 and Windows Server 2012 R2, use <a href="/windows/desktop/NativeWiFi/about-the-wi-fi-direct-api">Wi-Fi Direct</a> instead.</div><div> </div>

## -inheritance

The <b>IDot11AdHocNetworkNotificationSink</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDot11AdHocNetworkNotificationSink</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/adhoc/nn-adhoc-idot11adhocnetwork">IDot11AdHocNetwork</a>
