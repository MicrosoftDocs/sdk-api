---
UID: NF:faxcomex.IFaxOutboundRoutingGroups.Add
title: IFaxOutboundRoutingGroups::Add (faxcomex.h)
description: The IFaxOutboundRoutingGroups::Add method adds an outbound routing group to the collection represented by the IFaxOutboundRoutingGroups interface.
helpviewer_keywords: ["Add","Add method [Fax Service]","Add method [Fax Service]","IFaxOutboundRoutingGroups interface","IFaxOutboundRoutingGroups interface [Fax Service]","Add method","IFaxOutboundRoutingGroups.Add","IFaxOutboundRoutingGroups::Add","_mfax_faxoutboundroutinggroups.add_cpp","fax._mfax_faxoutboundroutinggroups_add_cpp","faxcomex/IFaxOutboundRoutingGroups::Add"]
old-location: fax\_mfax_faxoutboundroutinggroups_add_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_35r8_cpp.htm
ms.date: 12/05/2018
ms.keywords: Add, Add method [Fax Service], Add method [Fax Service],IFaxOutboundRoutingGroups interface, IFaxOutboundRoutingGroups interface [Fax Service],Add method, IFaxOutboundRoutingGroups.Add, IFaxOutboundRoutingGroups::Add, _mfax_faxoutboundroutinggroups.add_cpp, fax._mfax_faxoutboundroutinggroups_add_cpp, faxcomex/IFaxOutboundRoutingGroups::Add
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
 - IFaxOutboundRoutingGroups::Add
 - faxcomex/IFaxOutboundRoutingGroups::Add
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
 - IFaxOutboundRoutingGroups.Add
---

# IFaxOutboundRoutingGroups::Add


## -description

The <b>IFaxOutboundRoutingGroups::Add</b> method adds an outbound routing group to the collection represented by the <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutboundroutinggroups">IFaxOutboundRoutingGroups</a> interface.

## -parameters

### -param bstrName [in]

Type: <b>BSTR</b>

Null-terminated string that indicates the name of the group to add. Note that you cannot add the special <b>All Devices</b> routing group.

### -param pFaxOutboundRoutingGroup [out, retval]

Type: <b><a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutboundroutinggroup">IFaxOutboundRoutingGroup</a>**</b>

Address of a pointer that receives a <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutboundroutinggroup">IFaxOutboundRoutingGroup</a> interface.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To use this method, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farMANAGE_CONFIG</a> access right.

## -see-also

<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutboundroutinggroups">IFaxOutboundRoutingGroups</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-managing-outbound-routing-groups">Visual Basic Example</a>