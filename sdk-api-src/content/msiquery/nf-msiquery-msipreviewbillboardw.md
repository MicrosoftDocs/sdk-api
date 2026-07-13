---
UID: NF:msiquery.MsiPreviewBillboardW
title: MsiPreviewBillboardW function (msiquery.h)
description: The MsiPreviewBillboard function displays a billboard with the host control in the displayed dialog box. (Unicode)
helpviewer_keywords: ["MsiPreviewBillboard", "MsiPreviewBillboard function", "MsiPreviewBillboardW", "_msi_msipreviewbillboard", "msiquery/MsiPreviewBillboard", "msiquery/MsiPreviewBillboardW", "setup.msipreviewbillboard"]
old-location: setup\msipreviewbillboard.htm
tech.root: setup
ms.assetid: 7404ea12-bb38-4b7d-986e-2dff2fc36346
ms.date: 12/05/2018
ms.keywords: MsiPreviewBillboard, MsiPreviewBillboard function, MsiPreviewBillboardA, MsiPreviewBillboardW, _msi_msipreviewbillboard, msiquery/MsiPreviewBillboard, msiquery/MsiPreviewBillboardA, msiquery/MsiPreviewBillboardW, setup.msipreviewbillboard
req.header: msiquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiPreviewBillboardW (Unicode) and MsiPreviewBillboardA (ANSI)
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
 - MsiPreviewBillboardW
 - msiquery/MsiPreviewBillboardW
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
 - MsiPreviewBillboard
 - MsiPreviewBillboardA
 - MsiPreviewBillboardW
---

# MsiPreviewBillboardW function


## -description

The 
<b>MsiPreviewBillboard</b> function displays a billboard with the host control in the displayed dialog box.

## -parameters

### -param hPreview [in]

Handle to the preview.

### -param szControlName [in]

Specifies the name of the host control.

### -param szBillboard [in]

Specifies the name of the billboard to display.

## -returns

This function returns UINT.

## -remarks

Supplying a null billboard name in the 
<b>MsiPreviewBillboard</b> function removes any billboard displayed.





> [!NOTE]
> The msiquery.h header defines MsiPreviewBillboard as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Msi/database-functions">User Interface Functions</a>
