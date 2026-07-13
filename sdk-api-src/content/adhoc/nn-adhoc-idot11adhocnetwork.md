---
UID: NN:adhoc.IDot11AdHocNetwork
title: IDot11AdHocNetwork (adhoc.h)
description: Represents an available ad hoc network destination within connection range.
helpviewer_keywords: ["IDot11AdHocNetwork","IDot11AdHocNetwork interface [NativeWIFI]","IDot11AdHocNetwork interface [NativeWIFI]","described","adhoc/IDot11AdHocNetwork","nwifi.idot11adhocnetwork"]
old-location: nwifi\idot11adhocnetwork.htm
tech.root: nwifi
ms.assetid: 2736bb81-b66f-4c09-8c76-ca16f3eab192
ms.date: 12/05/2018
ms.keywords: IDot11AdHocNetwork, IDot11AdHocNetwork interface [NativeWIFI], IDot11AdHocNetwork interface [NativeWIFI],described, adhoc/IDot11AdHocNetwork, nwifi.idot11adhocnetwork
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
 - IDot11AdHocNetwork
 - adhoc/IDot11AdHocNetwork
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
 - IDot11AdHocNetwork
---

# IDot11AdHocNetwork interface


## -description

The <b>IDot11AdHocNetwork</b> interface represents an available ad hoc network destination within connection range. Before an application can connect to a network, the network must have been created using <a href="/windows/desktop/api/adhoc/nf-adhoc-idot11adhocmanager-createnetwork">IDot11AdHocManager::CreateNetwork</a> and committed using <a href="/windows/desktop/api/adhoc/nf-adhoc-idot11adhocmanager-commitcreatednetwork">IDot11AdHocManager::CommitCreatedNetwork</a>.
<div class="alert"><b>Note</b>  Ad hoc mode might not be available in future versions of Windows. Starting with Windows 8.1 and Windows Server 2012 R2, use <a href="/windows/desktop/NativeWiFi/about-the-wi-fi-direct-api">Wi-Fi Direct</a> instead.</div><div> </div>

## -inheritance

The <b>IDot11AdHocNetwork</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDot11AdHocNetwork</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/adhoc/nn-adhoc-idot11adhocmanager">IDot11AdHocManager</a>
