---
UID: NF:msiquery.MsiPreviewDialogW
title: MsiPreviewDialogW function (msiquery.h)
author: windows-sdk-content
description: The MsiPreviewDialog function displays a dialog box as modeless and inactive.
old-location: setup\msipreviewdialog.htm
tech.root: Msi
ms.assetid: 4017e122-8214-4158-ade3-5dac1fda428a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MsiPreviewDialog, MsiPreviewDialog function, MsiPreviewDialogA, MsiPreviewDialogW, _msi_msipreviewdialog, msiquery/MsiPreviewDialog, msiquery/MsiPreviewDialogA, msiquery/MsiPreviewDialogW, setup.msipreviewdialog
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
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msi.dll
api_name:
 - MsiPreviewDialog
 - MsiPreviewDialogA
 - MsiPreviewDialogW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/windows/desktop/Msi/database-functions">User Interface Functions</a>
 

 

