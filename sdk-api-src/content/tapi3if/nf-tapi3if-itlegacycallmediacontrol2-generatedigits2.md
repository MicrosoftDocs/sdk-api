---
UID: NF:tapi3if.ITLegacyCallMediaControl2.GenerateDigits2
title: ITLegacyCallMediaControl2::GenerateDigits2
author: windows-sdk-content
description: The GenerateDigits2 method causes digits to be output on the current call. This method extends the ITLegacyCallMediaControl::GenerateDigits method by adding a duration parameter.
old-location: tapi3\itlegacycallmediacontrol2_generatedigits2.htm
tech.root: tapi
ms.assetid: 63ea18ef-18ca-4771-a7d9-60d4e8c514a5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GenerateDigits2, GenerateDigits2 method [TAPI 2.2], GenerateDigits2 method [TAPI 2.2],ITLegacyCallMediaControl2 interface, ITLegacyCallMediaControl2 interface [TAPI 2.2],GenerateDigits2 method, ITLegacyCallMediaControl2.GenerateDigits2, ITLegacyCallMediaControl2::GenerateDigits2, _tapi3_itlegacycallmediacontrol2_generatedigits2, tapi3.itlegacycallmediacontrol2_generatedigits2, tapi3if/ITLegacyCallMediaControl2::GenerateDigits2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tapi3if.h
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITLegacyCallMediaControl2.GenerateDigits2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITLegacyCallMediaControl2::GenerateDigits2


## -description


The 
<b>GenerateDigits2</b> method causes digits to be output on the current call. This method extends the 
<a href="https://msdn.microsoft.com/d4dcdce0-4df5-43bb-a5ea-ea72782d5f04">ITLegacyCallMediaControl::GenerateDigits</a> method by adding a duration parameter.


## -parameters




### -param pDigits [in]

A pointer to a <b>BSTR</b> representation of the digits to generate.


### -param DigitMode [in]

Indicates the digit mode. Valid values are those from the TAPI 2.<i>x</i>
<a href="https://msdn.microsoft.com/d603ea28-2b93-4548-bb16-78e93087f828">LINEDIGITMODE_constants</a>.


### -param lDuration [in]

Both the duration, in milliseconds, of DTMF digits and pulse, and DTMF interdigit spacing.


## -returns



This method can return one of these values.

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
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pDigits</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TAPI_E_INVALCALLSTATE</b></dt>
</dl>
</td>
<td width="60%">
The call must be in the <i>connected</i> state.

</td>
</tr>
</table>
 




## -remarks



This method translates to a call to the TAPI 2.<i>x</i>
<a href="https://msdn.microsoft.com/aa407269-06be-43e2-906e-20137e4bdb89">lineGenerateDigits</a> function.

When digit generation finishes, an event of type TE_GENERATEEVENT is generated.




## -see-also




<a href="https://msdn.microsoft.com/47fa5669-1c74-4c18-8370-3efe35b3573e">ITLegacyCallMediaControl2</a>
 

 

