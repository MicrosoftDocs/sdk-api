---
UID: NF:msiquery.MsiPreviewDialogW
title: MsiPreviewDialogW function
author: windows-driver-content
description: The MsiPreviewDialog function displays a dialog box as modeless and inactive.
old-location: setup\msipreviewdialog.htm
old-project: Msi
ms.assetid: 4017e122-8214-4158-ade3-5dac1fda428a
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: MsiPreviewDialog, MsiPreviewDialog function, MsiPreviewDialogA, MsiPreviewDialogW, _msi_msipreviewdialog, msiquery/MsiPreviewDialog, msiquery/MsiPreviewDialogA, msiquery/MsiPreviewDialogW, setup.msipreviewdialog
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: msiquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiPreviewDialogW (Unicode) and MsiPreviewDialogA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: InkRecoGuide
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Msi.dll
api_name:
-	MsiPreviewDialog
-	MsiPreviewDialogA
-	MsiPreviewDialogW
product: Windows
targetos: Windows
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# MsiPreviewDialogW function


## -description


The 
<b>MsiPreviewDialog</b> function displays a dialog box as modeless and inactive.


## -parameters




### -param hPreview [in]

Handle to the preview.


### -param szDialogName [in]

Specifies the name of the dialog box to preview.


## -returns



This function returns UINT.




## -remarks



Supplying a null name in the 
<b>MsiPreviewDialog</b> function removes any current dialog box.




## -see-also




<a href="database_functions.htm">User Interface Functions</a>
 

 

