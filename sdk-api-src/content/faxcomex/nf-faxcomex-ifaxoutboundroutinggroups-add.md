---
UID: NF:faxcomex.IFaxOutboundRoutingGroups.Add
title: IFaxOutboundRoutingGroups::Add
author: windows-sdk-content
description: The IFaxOutboundRoutingGroups::Add method adds an outbound routing group to the collection represented by the IFaxOutboundRoutingGroups interface.
old-location: fax\_mfax_faxoutboundroutinggroups_add_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_35r8_cpp.htm
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: Add, Add method [Fax Service], Add method [Fax Service],IFaxOutboundRoutingGroups interface, IFaxOutboundRoutingGroups interface [Fax Service],Add method, IFaxOutboundRoutingGroups.Add, IFaxOutboundRoutingGroups::Add, _mfax_faxoutboundroutinggroups.add_cpp, fax._mfax_faxoutboundroutinggroups_add_cpp, faxcomex/IFaxOutboundRoutingGroups::Add
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - IFaxOutboundRoutingGroups.Add
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxOutboundRoutingGroups::Add


## -description


The <b>IFaxOutboundRoutingGroups::Add</b> method adds an outbound routing group to the collection represented by the <a href="https://msdn.microsoft.com/en-us/library/ms689212(v=VS.85).aspx">IFaxOutboundRoutingGroups</a> interface.


## -parameters




### -param bstrName [in]

Type: <b>BSTR</b>

Null-terminated string that indicates the name of the group to add. Note that you cannot add the special <b>All Devices</b> routing group.


### -param pFaxOutboundRoutingGroup [out, retval]

Type: <b><a href="https://msdn.microsoft.com/147fbebd-0000-4a24-b9cf-da4132b46edf">IFaxOutboundRoutingGroup</a>**</b>

Address of a pointer that receives a <a href="https://msdn.microsoft.com/147fbebd-0000-4a24-b9cf-da4132b46edf">IFaxOutboundRoutingGroup</a> interface.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To use this method, a user must have the <a href="https://msdn.microsoft.com/en-us/library/ms689205(v=VS.85).aspx">farMANAGE_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms689212(v=VS.85).aspx">IFaxOutboundRoutingGroups</a>



<a href="https://msdn.microsoft.com/en-us/library/ms693408(v=VS.85).aspx">Visual Basic Example</a>
 

 

