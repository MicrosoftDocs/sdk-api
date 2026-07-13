---
UID: NF:winscard.SCardIntroduceReaderA
title: SCardIntroduceReaderA function (winscard.h)
description: Introduces a new name for an existing smart card reader. (ANSI)
helpviewer_keywords: ["SCardIntroduceReaderA", "winscard/SCardIntroduceReaderA"]
old-location: security\scardintroducereader.htm
tech.root: security
ms.assetid: 1f8b9d75-5bba-40c3-99a0-6910855fcd4d
ms.date: 12/05/2018
ms.keywords: SCardIntroduceReader, SCardIntroduceReader function [Security], SCardIntroduceReaderA, SCardIntroduceReaderW, _smart_scardintroducereader, security.scardintroducereader, winscard/SCardIntroduceReader, winscard/SCardIntroduceReaderA, winscard/SCardIntroduceReaderW
req.header: winscard.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SCardIntroduceReaderW (Unicode) and SCardIntroduceReaderA (ANSI)
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
 - SCardIntroduceReaderA
 - winscard/SCardIntroduceReaderA
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
 - SCardIntroduceReader
 - SCardIntroduceReaderA
 - SCardIntroduceReaderW
---

# SCardIntroduceReaderA function


## -description

The <b>SCardIntroduceReader</b> function introduces a new name for an existing <a href="/windows/desktop/SecGloss/s-gly">smart card</a> <a href="/windows/desktop/SecGloss/r-gly">reader</a>.
<div class="alert"><b>Note</b>  Smart card readers are automatically introduced to the system; a smart card reader vendor's setup program can also introduce a smart card reader to the system.</div><div> </div>

## -parameters

### -param hContext [in]

Handle that identifies the <a href="/windows/desktop/SecGloss/r-gly">resource manager context</a>. The resource manager context is set by a previous call to 
<a href="/windows/desktop/api/winscard/nf-winscard-scardestablishcontext">SCardEstablishContext</a>. This parameter cannot be <b>NULL</b>.

### -param szReaderName [in]

Display name to be assigned to the reader.

### -param szDeviceName [in]

System name of the smart card reader, for example, "MyReader 01".

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

All readers installed on the system are automatically introduced by their system name. Typically, <b>SCardIntroduceReader</b> is called only to change the name of an existing reader.

The <b>SCardIntroduceReader</b> function is a database management function. For more information on other database management functions, see 
<a href="/windows/desktop/SecAuthN/smart-card-database-management-functions">Smart Card Database Management Functions</a>.

To remove a reader, use 
<a href="/windows/desktop/api/winscard/nf-winscard-scardforgetreadera">SCardForgetReader</a>.


#### Examples

The following example  shows introducing a smart card reader.


```cpp
// This example renames the reader name.
// This is a two-step process (first add the new
// name, then forget the old name).
LPBYTE    pbAttr = NULL;
DWORD     cByte = SCARD_AUTOALLOCATE;
LONG      lReturn;

// Step 1: Add the new reader name.
// The device name attribute is a necessary value.
// hCardHandle was set by a previous call to SCardConnect.
lReturn = SCardGetAttrib(hCardHandle,
                         SCARD_ATTR_DEVICE_SYSTEM_NAME,
                         (LPBYTE)&pbAttr,
                         &cByte);
if ( SCARD_S_SUCCESS != lReturn )
{
    printf("Failed SCardGetAttrib\n");
    exit(1);  // Or other error action
}
// Add the reader name.
// hContext was set earlier by SCardEstablishContext.
lReturn = SCardIntroduceReader(hContext,
                               TEXT("My New Reader Name"),
                               (LPCTSTR)pbAttr );
if ( SCARD_S_SUCCESS != lReturn )
{
    printf("Failed SCardIntroduceReader\n");
    exit(1);  // Or other error action
}

// Step 2: Forget the old reader name.
lReturn = SCardForgetReader(hContext,
                            (LPCTSTR)pbAttr );
if ( SCARD_S_SUCCESS != lReturn )
{
    printf("Failed SCardForgetReader\n");
    exit(1);  // Or other error action
}

// Free the memory when done.
lReturn = SCardFreeMemory( hContext, pbAttr );

```






> [!NOTE]
> The winscard.h header defines SCardIntroduceReader as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winscard/nf-winscard-scardestablishcontext">SCardEstablishContext</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scardforgetreadera">SCardForgetReader</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scardintroducecardtypea">SCardIntroduceCardType</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scardintroducereadergroupa">SCardIntroduceReaderGroup</a>
