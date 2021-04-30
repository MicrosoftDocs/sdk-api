---
UID: NF:winscard.SCardSetAttrib
title: SCardSetAttrib function (winscard.h)
description: Sets the given reader attribute for the given handle.
helpviewer_keywords: ["SCARD_ATTR_SUPRESS_T1_IFS_REQUEST","SCardSetAttrib","SCardSetAttrib function [Security]","_smart_scardsetattrib","security.scardsetattrib","winscard/SCardSetAttrib"]
old-location: security\scardsetattrib.htm
tech.root: security
ms.assetid: 755b9295-5daf-4e85-9e09-cce3a0e39c0b
ms.date: 12/05/2018
ms.keywords: SCARD_ATTR_SUPRESS_T1_IFS_REQUEST, SCardSetAttrib, SCardSetAttrib function [Security], _smart_scardsetattrib, security.scardsetattrib, winscard/SCardSetAttrib
req.header: winscard.h
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
req.lib: Winscard.lib
req.dll: Winscard.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SCardSetAttrib
 - winscard/SCardSetAttrib
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winscard.dll
api_name:
 - SCardSetAttrib
---

# SCardSetAttrib function


## -description

The <b>SCardSetAttrib</b> function sets the given <a href="/windows/desktop/SecGloss/r-gly">reader</a> attribute for the given handle. It does not affect the <a href="/windows/desktop/SecGloss/s-gly">state</a> of the <a href="/windows/desktop/SecGloss/r-gly">reader</a>, <a href="/windows/desktop/SecGloss/r-gly">reader driver</a>, or <a href="/windows/desktop/SecGloss/s-gly">smart card</a>. Not all attributes are supported by all readers (nor can they be set at all times) as many of the attributes are under direct control of the transport protocol.

## -parameters

### -param hCard [in]

Reference value returned from 
<a href="/windows/desktop/api/winscard/nf-winscard-scardconnecta">SCardConnect</a>.

### -param dwAttrId [in]

Identifier for the attribute to set. The values are write-only. Note that vendors may not support all attributes. 




					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SCARD_ATTR_SUPRESS_T1_IFS_REQUEST"></a><a id="scard_attr_supress_t1_ifs_request"></a><dl>
<dt><b>SCARD_ATTR_SUPRESS_T1_IFS_REQUEST</b></dt>
</dl>
</td>
<td width="60%">
Suppress sending of <a href="/windows/desktop/SecGloss/t-gly">T=1</a> IFSD packet from the reader to the card. (Can be used if the currently inserted card does not support an IFSD request.)

</td>
</tr>
</table>

### -param pbAttr [in]

Pointer to a buffer that supplies the attribute whose ID is supplied in <i>dwAttrId</i>.

### -param cbAttrLen [in]

Length (in bytes) of the attribute value in the <i>pbAttr</i> buffer.

## -returns

This function returns different values depending on whether it succeeds or fails.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Success</b></dt>
</dl>
</td>
<td width="60%">
SCARD_S_SUCCESS.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Failure</b></dt>
</dl>
</td>
<td width="60%">
An error code. For more information, see 
<a href="/windows/desktop/SecAuthN/authentication-return-values">Smart Card Return Values</a>.

</td>
</tr>
</table>

## -remarks

The <b>SCardSetAttrib</b> function is a direct card access function. For information about other direct access functions, see 
<a href="/windows/desktop/SecAuthN/direct-card-access-functions">Direct Card Access Functions</a>.


#### Examples

The following example  shows how to set an attribute.


```cpp
// Set the attribute.
// hCardHandle was set by a previous call to SCardConnect.
// dwAttrID is a DWORD value, specifying the attribute ID.
// pbAttr points to the buffer of the new value.
// cByte is the count of bytes in the buffer.
lReturn = SCardSetAttrib(hCardHandle,
                         dwAttrID,
                         (LPBYTE)pbAttr,
                         cByte);
if ( SCARD_S_SUCCESS != lReturn )
    printf("Failed SCardSetAttrib\n");

```

## -see-also

<a href="/windows/desktop/api/winscard/nf-winscard-scardconnecta">SCardConnect</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scardgetattrib">SCardGetAttrib</a>