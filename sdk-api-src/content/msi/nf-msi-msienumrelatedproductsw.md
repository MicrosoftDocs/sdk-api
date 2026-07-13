---
UID: NF:msi.MsiEnumRelatedProductsW
title: MsiEnumRelatedProductsW function (msi.h)
description: The MsiEnumRelatedProducts function enumerates products with a specified upgrade code. This function lists the currently installed and advertised products that have the specified UpgradeCode property in their Property table. (Unicode)
helpviewer_keywords: ["MsiEnumRelatedProducts", "MsiEnumRelatedProducts function", "MsiEnumRelatedProductsW", "_msi_msienumrelatedproducts", "msi/MsiEnumRelatedProducts", "msi/MsiEnumRelatedProductsW", "setup.msienumrelatedproducts"]
old-location: setup\msienumrelatedproducts.htm
tech.root: setup
ms.assetid: cb0fbdce-0b20-4fb3-8b01-d5e81d7bf3a3
ms.date: 12/05/2018
ms.keywords: MsiEnumRelatedProducts, MsiEnumRelatedProducts function, MsiEnumRelatedProductsA, MsiEnumRelatedProductsW, _msi_msienumrelatedproducts, msi/MsiEnumRelatedProducts, msi/MsiEnumRelatedProductsA, msi/MsiEnumRelatedProductsW, setup.msienumrelatedproducts
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiEnumRelatedProductsW (Unicode) and MsiEnumRelatedProductsA (ANSI)
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
 - MsiEnumRelatedProductsW
 - msi/MsiEnumRelatedProductsW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msi.dll
api_name:
 - MsiEnumRelatedProducts
 - MsiEnumRelatedProductsA
 - MsiEnumRelatedProductsW
---

# MsiEnumRelatedProductsW function


## -description

The 
<b>MsiEnumRelatedProducts</b> function enumerates products with a specified upgrade code. This function lists the currently installed and advertised products that have the specified 
<a href="/windows/desktop/Msi/upgradecode">UpgradeCode</a> property in their 
<a href="/windows/desktop/Msi/property-table">Property table</a>.

## -parameters

### -param lpUpgradeCode [in]

The null-terminated string specifying the upgrade code of related products that the installer is to enumerate.

### -param dwReserved [in]

This parameter is reserved and must be 0.

### -param iProductIndex [in]

The zero-based index into the registered products.

### -param lpProductBuf [out]

A buffer to receive the product code GUID. This buffer must be 39 characters long. The first 38 characters are for the 
<a href="/windows/desktop/Msi/guid">GUID</a>, and the last character is for the terminating null character.

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
The system does not have enough memory to complete the operation. Available starting with Windows Server 2003.

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

See 
<a href="/windows/desktop/Msi/upgradecode">UpgradeCode</a> property.

To enumerate currently installed and advertised products that have a specific upgrade code, an application should initially call the 
<b>MsiEnumRelatedProducts</b> function with the <i>iProductIndex</i> parameter set to zero. The application should then increment the <i>iProductIndex</i> parameter and call 
<b>MsiEnumRelatedProducts</b> until the function returns ERROR_NO_MORE_ITEMS, which means there are no more products with the specified upgrade code.

When making multiple calls to 
<b>MsiEnumRelatedProducts</b> to enumerate all of the related products, each call should be made from the same thread.




> [!NOTE]
> The msi.h header defines MsiEnumRelatedProducts as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
