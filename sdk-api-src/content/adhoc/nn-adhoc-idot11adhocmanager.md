---
UID: NN:adhoc.IDot11AdHocManager
title: IDot11AdHocManager (adhoc.h)
description: Creates and manages 802.11 ad hoc networks.
helpviewer_keywords: ["IDot11AdHocManager","IDot11AdHocManager interface [NativeWIFI]","IDot11AdHocManager interface [NativeWIFI]","described","adhoc/IDot11AdHocManager","nwifi.idot11adhocmanager"]
old-location: nwifi\idot11adhocmanager.htm
tech.root: nwifi
ms.assetid: dcb93b9c-3292-4cbf-9d44-5367bdbd4878
ms.date: 12/05/2018
ms.keywords: IDot11AdHocManager, IDot11AdHocManager interface [NativeWIFI], IDot11AdHocManager interface [NativeWIFI],described, adhoc/IDot11AdHocManager, nwifi.idot11adhocmanager
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
 - IDot11AdHocManager
 - adhoc/IDot11AdHocManager
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
 - IDot11AdHocManager
---

# IDot11AdHocManager interface


## -description

The <b>IDot11AdHocManager</b> interface creates and manages 802.11 ad hoc networks.  It is the top-level 802.11 ad hoc interface and the only ad hoc interface with a coclass. As such, it is the only ad hoc interface that can be instantiated by <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a>. 
<div class="alert"><b>Note</b>  Ad hoc mode might not be available in future versions of Windows. Starting with Windows 8.1 and Windows Server 2012 R2, use <a href="/windows/desktop/NativeWiFi/about-the-wi-fi-direct-api">Wi-Fi Direct</a> instead.</div><div> </div>The <b>IDot11AdHocManager</b> coclass implements the <a href="/windows/desktop/api/ocidl/nn-ocidl-iconnectionpoint">IConnectionPoint</a> interface. The <a href="/windows/desktop/api/ocidl/nf-ocidl-iconnectionpoint-advise">Advise</a> method can be used to register for network manager, network, and interface-related notifications. Notifications are implemented by the <a href="/windows/desktop/api/adhoc/nn-adhoc-idot11adhocmanagernotificationsink">IDot11AdHocManagerNotificationSink</a> interface. To register for notifications, call the <b>Advise</b> method with the appropriate notification sink interface as the <i>pUnk</i>  parameter.

## -inheritance

The <b>IDot11AdHocManager</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDot11AdHocManager</b> also has these types of members:

