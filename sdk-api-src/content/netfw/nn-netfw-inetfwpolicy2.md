---
UID: NN:netfw.INetFwPolicy2
title: INetFwPolicy2 (netfw.h)
description: To access the firewall policy.
helpviewer_keywords: ["INetFwPolicy2","INetFwPolicy2 interface [ICS/ICF]","INetFwPolicy2 interface [ICS/ICF]","described","ics.inetfwpolicy2","netfw/INetFwPolicy2"]
old-location: ics\inetfwpolicy2.htm
tech.root: ics
ms.assetid: ef01a531-ddb0-4eb4-894b-82f613016396
ms.date: 12/05/2018
ms.keywords: INetFwPolicy2, INetFwPolicy2 interface [ICS/ICF], INetFwPolicy2 interface [ICS/ICF],described, ics.inetfwpolicy2, netfw/INetFwPolicy2
req.header: netfw.h
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
req.dll: FirewallAPI.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - INetFwPolicy2
 - netfw/INetFwPolicy2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FirewallAPI.dll
api_name:
 - INetFwPolicy2
---

# INetFwPolicy2 interface


## -description

The <b>INetFwPolicy2</b> interface allows an application or service to access the firewall policy.

## -inheritance

The <b>INetFwPolicy2</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>INetFwPolicy2</b> also has these types of members:

## -remarks

All configuration changes take effect immediately.

The Windows Firewall/Internet Connection Sharing  service must be running to access this interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
