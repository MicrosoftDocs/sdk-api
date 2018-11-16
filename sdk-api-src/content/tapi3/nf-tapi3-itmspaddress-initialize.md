---
UID: NF:tapi3.ITMSPAddress.Initialize
title: ITMSPAddress::Initialize
author: windows-sdk-content
description: The Initialize method is called when the MSP is loaded.
old-location: tapi3\itmspaddress_initialize.htm
tech.root: Tapi
ms.assetid: 5df2c486-0133-4705-8d37-10b56b40c85d
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ITMSPAddress interface [TAPI 2.2],Initialize method, ITMSPAddress.Initialize, ITMSPAddress::Initialize, Initialize, Initialize method [TAPI 2.2], Initialize method [TAPI 2.2],ITMSPAddress interface, _tapi3_itmspaddress_initialize, msp/ITMSPAddress::Initialize, tapi3.itmspaddress_initialize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tapi3.h
req.include-header: Tapi3.h
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
 - msp.h
api_name:
 - ITMSPAddress.Initialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- tapi3.h
: 
- ITMSPAddress.Initialize
: 
---

# ITMSPAddress::Initialize


## -description


The 
<b>Initialize</b> method is called when the MSP is loaded.


## -parameters




### -param hEvent [in]

TAPI 3's handle for this MSP.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform operation.

</td>
</tr>
</table>
 




## -remarks



If an MSP is written using the MSP base classes, this method initializes data members, creates the Terminal Manager, and calls Start on the global MSP thread object.




## -see-also




<a href="https://msdn.microsoft.com/246a0bcd-0dbb-4b77-a1cd-e6378eaff889">ITMSPAddress</a>



<a href="https://msdn.microsoft.com/53b7bcbd-571a-44da-a6db-10d4c3e5d30a">Media Service Provider Interface (MSPI)</a>
 

 

