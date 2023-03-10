---
UID: NN:netfw.INetFwServiceRestriction
title: INetFwServiceRestriction (netfw.h)
description: Access to the Windows Service Hardening networking rules.
helpviewer_keywords: ["INetFwServiceRestriction","INetFwServiceRestriction interface [ICS/ICF]","INetFwServiceRestriction interface [ICS/ICF]","described","ics.inetfwservicerestriction","netfw/INetFwServiceRestriction"]
old-location: ics\inetfwservicerestriction.htm
tech.root: ics
ms.assetid: e426cae9-8c39-44cf-bd48-3b385fdfbdf7
ms.date: 12/05/2018
ms.keywords: INetFwServiceRestriction, INetFwServiceRestriction interface [ICS/ICF], INetFwServiceRestriction interface [ICS/ICF],described, ics.inetfwservicerestriction, netfw/INetFwServiceRestriction
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
 - INetFwServiceRestriction
 - netfw/INetFwServiceRestriction
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
 - INetFwServiceRestriction
---

# INetFwServiceRestriction interface


## -description

The <b>INetFwServiceRestriction</b> interface provides access to the Windows Service Hardening networking rules.

## -inheritance

The <b>INetFwServiceRestriction</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>INetFwServiceRestriction</b> also has these types of members:

## -remarks

When adding rules, note that there may be a small time lag before the newly-added rule is applied.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
