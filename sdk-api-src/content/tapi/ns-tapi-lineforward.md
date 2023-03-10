---
UID: NS:tapi.lineforward_tag
title: LINEFORWARD (tapi.h)
description: The LINEFORWARD structure describes an entry of the forwarding instructions. The LINEFORWARDLIST and the LINEADDRESSSTATUS structures can contain an array of LINEFORWARD structures.
helpviewer_keywords: ["*LPLINEFORWARD","LINEFORWARD","LINEFORWARD structure [TAPI 2.2]","LINEFORWARDMODE_BUSYNASPECIFIC","LINEFORWARDMODE_BUSYSPECIFIC","LINEFORWARDMODE_NOANSWSPECIFIC","LINEFORWARDMODE_UNCONDSPECIFIC","LPLINEFORWARD","LPLINEFORWARD structure pointer [TAPI 2.2]","_tapi2_lineforward_str","tapi/LINEFORWARD","tapi/LPLINEFORWARD","tapi2.lineforward_str"]
old-location: tapi2\lineforward_str.htm
tech.root: tapi3
ms.assetid: cbdb4409-a51a-4ddf-b3ec-c5b958fc2527
ms.date: 12/05/2018
ms.keywords: '*LPLINEFORWARD, LINEFORWARD, LINEFORWARD structure [TAPI 2.2], LINEFORWARDMODE_BUSYNASPECIFIC, LINEFORWARDMODE_BUSYSPECIFIC, LINEFORWARDMODE_NOANSWSPECIFIC, LINEFORWARDMODE_UNCONDSPECIFIC, LPLINEFORWARD, LPLINEFORWARD structure pointer [TAPI 2.2], _tapi2_lineforward_str, tapi/LINEFORWARD, tapi/LPLINEFORWARD, tapi2.lineforward_str'
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
targetos: Windows
req.typenames: LINEFORWARD, *LPLINEFORWARD
req.redist: 
ms.custom: 19H1
f1_keywords:
 - lineforward_tag
 - tapi/lineforward_tag
 - LPLINEFORWARD
 - tapi/LPLINEFORWARD
 - LINEFORWARD
 - tapi/LINEFORWARD
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tapi.h
api_name:
 - LINEFORWARD
---

# LINEFORWARD structure


## -description

The 
<b>LINEFORWARD</b> structure describes an entry of the forwarding instructions. The 
<a href="/windows/desktop/api/tapi/ns-tapi-lineforwardlist">LINEFORWARDLIST</a> and the 
<a href="/windows/desktop/api/tapi/ns-tapi-lineaddressstatus">LINEADDRESSSTATUS</a> structures can contain an array of 
<b>LINEFORWARD</b> structures.

## -struct-fields

### -field dwForwardMode

Types of forwarding. This member uses one of the 
<a href="/windows/desktop/Tapi/lineforwardmode--constants">LINEFORWARDMODE_ Constants</a>.

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

<a href="/windows/desktop/Tapi/lineaddresstype--constants">Address type</a> of the caller. This member of the structure is available only if the negotiated version of TAPI is 3.1 or higher.

### -field dwDestAddressType

<a href="/windows/desktop/Tapi/lineaddresstype--constants">Address type</a> for the called destination. This member of the structure is available only if the negotiated version of TAPI is 3.1 or higher.

## -remarks

This structure may not be extended.

Each entry in the 
<b>LINEFORWARD</b> structure specifies a forwarding request.

## -see-also

<a href="/windows/desktop/api/tapi/ns-tapi-lineaddressstatus">LINEADDRESSSTATUS</a>



<a href="/windows/desktop/api/tapi/ns-tapi-lineforwardlist">LINEFORWARDLIST</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_lineforward">TSPI_lineForward</a>



<a href="/windows/desktop/api/tapi/nf-tapi-lineforward">lineForward</a>