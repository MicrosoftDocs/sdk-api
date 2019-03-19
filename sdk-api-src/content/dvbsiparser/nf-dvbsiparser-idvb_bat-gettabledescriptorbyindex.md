---
UID: NF:dvbsiparser.IDVB_BAT.GetTableDescriptorByIndex
title: IDVB_BAT::GetTableDescriptorByIndex (dvbsiparser.h)
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\idvb_bat_gettabledescriptorbyindex.htm
tech.root: mstv
ms.assetid: fa985aea-3822-439e-9a83-916cc1c9ae93
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetTableDescriptorByIndex, GetTableDescriptorByIndex method [Microsoft TV Technologies], GetTableDescriptorByIndex method [Microsoft TV Technologies],IDVB_BAT interface, IDVB_BAT interface [Microsoft TV Technologies],GetTableDescriptorByIndex method, IDVB_BAT.GetTableDescriptorByIndex, IDVB_BAT::GetTableDescriptorByIndex, IDVB_BATGetTableDescriptorByIndex, dvbsiparser/IDVB_BAT::GetTableDescriptorByIndex, mstv.idvb_bat_gettabledescriptorbyindex
ms.topic: method
req.header: dvbsiparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IDVB_BAT.GetTableDescriptorByIndex
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDVB_BAT::GetTableDescriptorByIndex


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetTableDescriptorByIndex</b> method retrieves a table-wide descriptor for the BAT.


## -parameters




### -param dwIndex [in]

Specifies which descriptor to retrieve, indexed from zero. Call the <a href="https://msdn.microsoft.com/8f373cbe-9d07-41c2-83a5-c25bc66f6263">IDVB_BAT::GetCountOfTableDescriptors</a> method to get the number of table descriptors in the BAT.


### -param ppDescriptor [in]

Address of a variable that receives an <a href="https://msdn.microsoft.com/en-us/library/Dd694093(v=VS.85).aspx">IGenericDescriptor</a> interface pointer. Use this interface to retrieve the information in the descriptor. The caller must release the interface.


## -returns



The method returns an <b>HRESULT</b>. Possible values include those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
NULL pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MPEG2_E_OUT_OF_BOUNDS</b></dt>
</dl>
</td>
<td width="60%">
Index out of bounds.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/c312a152-21ee-4708-90a8-ab9bde9a2011">IDVB_BAT Interface</a>
 

 

