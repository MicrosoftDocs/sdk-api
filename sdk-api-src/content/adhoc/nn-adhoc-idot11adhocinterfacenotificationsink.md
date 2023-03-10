---
UID: NN:adhoc.IDot11AdHocInterfaceNotificationSink
title: IDot11AdHocInterfaceNotificationSink (adhoc.h)
description: Defines the notifications supported by IDot11AdHocInterface.
helpviewer_keywords: ["IDot11AdHocInterfaceNotificationSink","IDot11AdHocInterfaceNotificationSink interface [NativeWIFI]","IDot11AdHocInterfaceNotificationSink interface [NativeWIFI]","described","adhoc/IDot11AdHocInterfaceNotificationSink","nwifi.idot11adhocinterfacenotificationsink"]
old-location: nwifi\idot11adhocinterfacenotificationsink.htm
tech.root: nwifi
ms.assetid: ab3fd026-32b4-48cb-aa10-37a084b5b08e
ms.date: 12/05/2018
ms.keywords: IDot11AdHocInterfaceNotificationSink, IDot11AdHocInterfaceNotificationSink interface [NativeWIFI], IDot11AdHocInterfaceNotificationSink interface [NativeWIFI],described, adhoc/IDot11AdHocInterfaceNotificationSink, nwifi.idot11adhocinterfacenotificationsink
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
 - IDot11AdHocInterfaceNotificationSink
 - adhoc/IDot11AdHocInterfaceNotificationSink
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
 - IDot11AdHocInterfaceNotificationSink
---

# IDot11AdHocInterfaceNotificationSink interface


## -description

The <b>IDot11AdHocInterfaceNotificationSink</b> interface defines the notifications supported by <a href="/windows/desktop/api/adhoc/nn-adhoc-idot11adhocinterface">IDot11AdHocInterface</a>. To register for notifications, call the  <a href="/windows/desktop/api/ocidl/nf-ocidl-iconnectionpoint-advise">Advise</a> method on an instantiated <a href="/windows/desktop/api/adhoc/nn-adhoc-idot11adhocmanager">IDot11AdHocManager</a> object with the <b>IDot11AdHocInterfaceNotificationSink</b> interface passed  as the <i>pUnk</i>  parameter.  To terminate notifications, call the <a href="/windows/desktop/api/ocidl/nf-ocidl-iconnectionpoint-unadvise">Unadvise</a> method.
<div class="alert"><b>Note</b>  Ad hoc mode might not be available in future versions of Windows. Starting with Windows 8.1 and Windows Server 2012 R2, use <a href="/windows/desktop/NativeWiFi/about-the-wi-fi-direct-api">Wi-Fi Direct</a> instead.</div><div> </div>

## -inheritance

The <b>IDot11AdHocInterfaceNotificationSink</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDot11AdHocInterfaceNotificationSink</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/adhoc/nn-adhoc-idot11adhocinterface">IDot11AdHocInterface</a>
