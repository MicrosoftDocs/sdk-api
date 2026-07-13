---
UID: NF:msi.MsiEnumProductsW
title: MsiEnumProductsW function (msi.h)
description: The MsiEnumProducts function enumerates through all the products currently advertised or installed. Products that are installed in both the per-user and per-machine installation context and advertisements are enumerated. (Unicode)
helpviewer_keywords: ["MsiEnumProducts", "MsiEnumProducts function", "MsiEnumProductsW", "_msi_msienumproducts", "msi/MsiEnumProducts", "msi/MsiEnumProductsW", "setup.msienumproducts"]
old-location: setup\msienumproducts.htm
tech.root: setup
ms.assetid: c05ddc32-2c61-49ab-991f-8f9efae331a4
ms.date: 12/05/2018
ms.keywords: MsiEnumProducts, MsiEnumProducts function, MsiEnumProductsA, MsiEnumProductsW, _msi_msienumproducts, msi/MsiEnumProducts, msi/MsiEnumProductsA, msi/MsiEnumProductsW, setup.msienumproducts
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiEnumProductsW (Unicode) and MsiEnumProductsA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MsiEnumProductsW
 - msi/MsiEnumProductsW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-msi-misc-l1-1-0.dll
 - Msi.dll
api_name:
 - MsiEnumProducts
 - MsiEnumProductsA
 - MsiEnumProductsW
---

# MsiEnumProductsW function


## -description

The 
<b>MsiEnumProducts</b> function enumerates through all the products currently advertised or installed. Products that are installed in both the per-user and per-machine <a href="/windows/desktop/Msi/installation-context">installation context</a> and advertisements are enumerated.

## -parameters

### -param iProductIndex [in]

Specifies the index of the product to retrieve. This parameter should be zero for the first call to the 
<b>MsiEnumProducts</b> function and then incremented for subsequent calls. Because products are not ordered, any new product has an arbitrary index. This means that the function can return products in any order.

### -param lpProductBuf [out]

Pointer to a buffer that receives the product code. This buffer must be 39 characters long. The first 38 characters are for the GUID, and the last character is for the terminating null character.

## -returns

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_CONFIGURATION</b></dt>
</dl>
</td>
<td width="60%">
The configuration data is corrupt.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was passed to the function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_MORE_ITEMS</b></dt>
</dl>
</td>
<td width="60%">
There are no products to return.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
The system does not have enough memory to complete the operation. Available with Windows Server 2003.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
A value was enumerated.

</td>
</tr>
</table>

## -remarks

To enumerate products, an application should initially call the 
<b>MsiEnumProducts</b> function with the <i>iProductIndex</i> parameter set to zero. The application should then increment the <i>iProductIndex</i> parameter and call 
<b>MsiEnumProducts</b> until there are no more products (until the function returns ERROR_NO_MORE_ITEMS).

When making multiple calls to 
<b>MsiEnumProducts</b> to enumerate all of the products, each call should be made from the same thread.





> [!NOTE]
> The msi.h header defines MsiEnumProducts as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Msi/determining-installation-context">Determining Installation Context</a>



<a href="/windows/desktop/Msi/installer-function-reference">System Status Functions</a>
