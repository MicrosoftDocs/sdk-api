---
UID: NF:faxcomex.IFaxOutboundRouting.GetGroups
title: IFaxOutboundRouting::GetGroups (faxcomex.h)
description: The IFaxOutboundRouting::GetGroups method retrieves an interface that represents a collection of outbound routing groups.
helpviewer_keywords: ["GetGroups","GetGroups method [Fax Service]","GetGroups method [Fax Service]","IFaxOutboundRouting interface","IFaxOutboundRouting interface [Fax Service]","GetGroups method","IFaxOutboundRouting.GetGroups","IFaxOutboundRouting::GetGroups","_mfax_faxoutboundrouting.getgroups_cpp","fax._mfax_faxoutboundrouting_getgroups_cpp","faxcomex/IFaxOutboundRouting::GetGroups"]
old-location: fax\_mfax_faxoutboundrouting_getgroups_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_8j1v_cpp.htm
ms.date: 12/05/2018
ms.keywords: GetGroups, GetGroups method [Fax Service], GetGroups method [Fax Service],IFaxOutboundRouting interface, IFaxOutboundRouting interface [Fax Service],GetGroups method, IFaxOutboundRouting.GetGroups, IFaxOutboundRouting::GetGroups, _mfax_faxoutboundrouting.getgroups_cpp, fax._mfax_faxoutboundrouting_getgroups_cpp, faxcomex/IFaxOutboundRouting::GetGroups
req.header: faxcomex.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - IFaxOutboundRouting::GetGroups
 - faxcomex/IFaxOutboundRouting::GetGroups
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
 - IFaxOutboundRouting.GetGroups
---

# IFaxOutboundRouting::GetGroups


## -description

The <b>IFaxOutboundRouting::GetGroups</b> method retrieves an interface that represents a collection of outbound routing groups.

## -parameters

### -param pFaxOutboundRoutingGroups [out, retval]

Type: <b><a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutboundroutinggroups">IFaxOutboundRoutingGroups</a>**</b>

An address of a pointer that receives an <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutboundroutinggroups">IFaxOutboundRoutingGroups</a> interface.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To use this method, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farQUERY_CONFIG</a> access right.

## -see-also

<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutboundrouting">IFaxOutboundRouting</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-managing-outbound-routing-groups">Visual Basic Example</a>