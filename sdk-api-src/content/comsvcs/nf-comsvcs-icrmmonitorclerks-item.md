---
UID: NF:comsvcs.ICrmMonitorClerks.Item
title: ICrmMonitorClerks::Item
author: windows-sdk-content
description: Retrieves the instance CLSID of the CRM clerk for the specified index.
old-location: cos\icrmmonitorclerks_item.htm
tech.root: cossdk
ms.assetid: af25d159-95e6-4695-9350-9a3c1bc034e9
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ICrmMonitorClerks interface [COM+],Item method, ICrmMonitorClerks.Item, ICrmMonitorClerks::Item, Item, Item method [COM+], Item method [COM+],ICrmMonitorClerks interface, _dtc_ICrmMonitorClerks_Item, comsvcs/ICrmMonitorClerks::Item, cos.icrmmonitorclerks_item
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - ComSvcs.h
api_name:
 - ICrmMonitorClerks.Item
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICrmMonitorClerks::Item


## -description


Retrieves the instance CLSID of the CRM clerk for the specified index.


## -parameters




### -param Index [in]

The index of the required CRM clerk as a numeric <b>Variant</b>.


### -param pItem [out]

A pointer to <b>Variant</b> string returning the instance CLSID corresponding to this numeric index.


## -returns



This method can return the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A <b>NULL</b> pointer was provided as an argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the arguments is incorrect.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/90403516-f677-4396-8991-ae621c159567">ICrmMonitorClerks</a>
 

 

