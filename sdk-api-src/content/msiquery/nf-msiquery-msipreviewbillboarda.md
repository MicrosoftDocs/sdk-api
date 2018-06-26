---
UID: NF:msiquery.MsiPreviewBillboardA
title: MsiPreviewBillboardA function
author: windows-sdk-content
description: The MsiPreviewBillboard function displays a billboard with the host control in the displayed dialog box.
old-location: setup\msipreviewbillboard.htm
old-project: Msi
ms.assetid: 7404ea12-bb38-4b7d-986e-2dff2fc36346
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: MsiPreviewBillboard, MsiPreviewBillboard function, MsiPreviewBillboardA, MsiPreviewBillboardW, _msi_msipreviewbillboard, msiquery/MsiPreviewBillboard, msiquery/MsiPreviewBillboardA, msiquery/MsiPreviewBillboardW, setup.msipreviewbillboard
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: InkRecoGuide
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
product: Windows
targetos: Windows
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# MsiPreviewBillboardA function


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




## -see-also




<a href="database_functions.htm">User Interface Functions</a>
 

 

