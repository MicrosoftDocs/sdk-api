---
UID: NF:netfw.INetFwProducts.Item
title: INetFwProducts::Item
author: windows-sdk-content
description: The Item method returns the product with the specified index if it is in the collection.
old-location: ics\inetfwproducts_item.htm
tech.root: ics
ms.assetid: 091d53bc-3c5e-4960-9bc9-34343fd352ce
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: INetFwProducts interface [ICS/ICF],Item method, INetFwProducts.Item, INetFwProducts::Item, Item, Item method [ICS/ICF], Item method [ICS/ICF],INetFwProducts interface, ics.inetfwproducts_item, netfw/INetFwProducts::Item
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: netfw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FirewallAPI.dll
api_name:
 - INetFwProducts.Item
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INetFwProducts::Item


## -description


The <b>Item</b> method returns the product with the specified index if it is in the collection.


## -parameters




### -param index [in]

Index of the product to retrieve.


### -param product [out, retval]

Reference to the returned <a href="https://msdn.microsoft.com/e4cadbfd-d48d-4b38-a068-fc005d6f72af">INetFwProduct</a> object.


## -returns



If the method succeeds the return value is S_OK.

If the method fails, the return value is one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The operation was aborted due to permissions issues.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The method failed due to an invalid parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method was unable to allocate required memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The method failed due to an invalid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND) </b></dt>
</dl>
</td>
<td width="60%">
The requested item does not exist.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/e4cadbfd-d48d-4b38-a068-fc005d6f72af">INetFwProduct</a>



<a href="https://msdn.microsoft.com/66608887-02df-4caf-91d0-e5091849ff32">INetFwProducts</a>
 

 

