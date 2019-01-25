---
UID: NS:tapi.lineforward_tag
title: LINEFORWARD
author: windows-sdk-content
description: The LINEFORWARD structure describes an entry of the forwarding instructions. The LINEFORWARDLIST and the LINEADDRESSSTATUS structures can contain an array of LINEFORWARD structures.
old-location: tapi2\lineforward_str.htm
tech.root: Tapi
ms.assetid: cbdb4409-a51a-4ddf-b3ec-c5b958fc2527
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPLINEFORWARD, LINEFORWARD, LINEFORWARD structure [TAPI 2.2], LINEFORWARDMODE_BUSYNASPECIFIC, LINEFORWARDMODE_BUSYSPECIFIC, LINEFORWARDMODE_NOANSWSPECIFIC, LINEFORWARDMODE_UNCONDSPECIFIC, LPLINEFORWARD, LPLINEFORWARD structure pointer [TAPI 2.2], _tapi2_lineforward_str, tapi/LINEFORWARD, tapi/LPLINEFORWARD, tapi2.lineforward_str"
ms.topic: struct
req.header: tapi.h
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
 - HeaderDef
api_location:
 - Tapi.h
api_name:
 - LINEFORWARD
product: Windows
targetos: Windows
req.typenames: LINEFORWARD, *LPLINEFORWARD
req.redist: 
---

# LINEFORWARD structure


## -description


The 
<b>LINEFORWARD</b> structure describes an entry of the forwarding instructions. The 
<a href="https://msdn.microsoft.com/3dec9ab6-43d8-4dda-b0b1-a25407e4d77a">LINEFORWARDLIST</a> and the 
<a href="https://msdn.microsoft.com/795aa97d-76a9-4041-b9f6-345644561043">LINEADDRESSSTATUS</a> structures can contain an array of 
<b>LINEFORWARD</b> structures.


## -struct-fields




### -field dwForwardMode

Types of forwarding. This member uses one of the 
<a href="https://msdn.microsoft.com/8cc053bd-1056-42be-b48a-d2312c456893">LINEFORWARDMODE_ Constants</a>.


### -field dwCallerAddressSize

Size of the variably sized field containing the address of a caller to be forwarded, in bytes. 


### -field dwCallerAddressOffset

Offset from the beginning of this structure to the variably sized field containing the address of a caller to be forwarded. This member is set to zero if <b>dwForwardMode</b> is not one of the following values:

<a id="LINEFORWARDMODE_BUSYNASPECIFIC"></a>
<a id="lineforwardmode_busynaspecific"></a>


#### LINEFORWARDMODE_BUSYNASPECIFIC

<a id="LINEFORWARDMODE_NOANSWSPECIFIC"></a>
<a id="lineforwardmode_noanswspecific"></a>


#### LINEFORWARDMODE_NOANSWSPECIFIC

<a id="LINEFORWARDMODE_UNCONDSPECIFIC"></a>
<a id="lineforwardmode_uncondspecific"></a>


#### LINEFORWARDMODE_UNCONDSPECIFIC

<a id="LINEFORWARDMODE_BUSYSPECIFIC"></a>
<a id="lineforwardmode_busyspecific"></a>


#### LINEFORWARDMODE_BUSYSPECIFIC

The size of the field is specified by <b>dwCallerAddressSize</b>.


### -field dwDestCountryCode

Country or region code of the destination address to which the call is to be forwarded.


### -field dwDestAddressSize

Size of the variably sized field containing the address of the address where calls are to be forwarded, in bytes.


### -field dwDestAddressOffset

Offset from the beginning of this structure to the variably sized field containing the address of the address where calls are to be forwarded. The size of the field is specified by <b>dwDestAddressSize</b>.


### -field dwCallerAddressType


<a href="https://msdn.microsoft.com/2c32eda1-e510-40eb-ae75-fc7b9e9953cd">Address type</a> of the caller. This member of the structure is available only if the negotiated version of TAPI is 3.1 or higher.


### -field dwDestAddressType


<a href="https://msdn.microsoft.com/2c32eda1-e510-40eb-ae75-fc7b9e9953cd">Address type</a> for the called destination. This member of the structure is available only if the negotiated version of TAPI is 3.1 or higher.


## -remarks



This structure may not be extended.

Each entry in the 
<b>LINEFORWARD</b> structure specifies a forwarding request.




## -see-also




<a href="https://msdn.microsoft.com/795aa97d-76a9-4041-b9f6-345644561043">LINEADDRESSSTATUS</a>



<a href="https://msdn.microsoft.com/3dec9ab6-43d8-4dda-b0b1-a25407e4d77a">LINEFORWARDLIST</a>



<a href="https://msdn.microsoft.com/fd70bf7f-653c-47db-bf81-6a620f47e5bc">TSPI_lineForward</a>



<a href="https://msdn.microsoft.com/68dc99c5-1158-4e18-8e32-08216ff3567b">lineForward</a>
 

 

