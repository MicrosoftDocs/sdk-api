---
UID: NF:faxcomex.IFaxOutboundRoutingGroups.Remove
title: IFaxOutboundRoutingGroups::Remove
author: windows-sdk-content
description: The Remove method removes an item from the FaxOutboundRoutingGroups collection.
old-location: fax\_mfax_faxoutboundroutinggroups_cpp_mfax_faxoutboundroutinggroups_remove_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_5h45.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFaxOutboundRoutingGroups interface [Fax Service],Remove method, IFaxOutboundRoutingGroups.Remove, IFaxOutboundRoutingGroups::Remove, Remove, Remove method [Fax Service], Remove method [Fax Service],IFaxOutboundRoutingGroups interface, _mfax_faxoutboundroutinggroups.remove, fax._mfax_faxoutboundroutinggroups_cpp_mfax_faxoutboundroutinggroups_remove_cpp, fax._mfax_faxoutboundroutinggroups_remove, faxcomex/IFaxOutboundRoutingGroups::Remove
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
 - IFaxOutboundRoutingGroups.Remove
 - IFaxOutboundRoutingGroups.Remove
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxOutboundRoutingGroups::Remove


## -description


The <b>Remove</b> method removes an item from the <a href="https://msdn.microsoft.com/en-us/library/ms689211(v=VS.85).aspx">FaxOutboundRoutingGroups</a> collection. 
<div class="alert"><b>Note</b>  You cannot remove the special <b>All Devices</b> routing group.</div><div> </div>

## -parameters




### -param vIndex

Type: <b>VARIANT</b>


<a href="https://msdn.microsoft.com/en-us/library/ms221627(v=VS.85).aspx">Variant</a> that specifies the item to remove from the collection.
				



If this parameter is type VT_I2 or VT_I4, it specifies the index of the item to remove from the collection. Valid values for this parameter are in the range from 1 to n, where n is the number of objects returned by a call to the <a href="https://msdn.microsoft.com/en-us/library/ms689185(v=VS.85).aspx">IFaxOutboundRoutingGroups::get_Count</a> method. The index is 1-based. If this parameter is type VT_BSTR, the parameter is a unique name that identifies the outbound routing group to remove. Other types are not supported.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To use this method, a user must have the <a href="https://msdn.microsoft.com/en-us/library/ms689205(v=VS.85).aspx">farMANAGE_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms689211(v=VS.85).aspx">FaxOutboundRoutingGroups</a>



<a href="https://msdn.microsoft.com/en-us/library/ms689212(v=VS.85).aspx">IFaxOutboundRoutingGroups</a>



<a href="https://msdn.microsoft.com/en-us/library/ms693408(v=VS.85).aspx">Visual Basic Example</a>
 

 

