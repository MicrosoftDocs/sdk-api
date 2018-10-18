---
UID: NF:shlobj.IShellFolderBand.SetBandInfoSFB
title: IShellFolderBand::SetBandInfoSFB
author: windows-sdk-content
description: Uses the information in a BANDINFOSFB structure to set the band information for a IShellFolderBand object.
old-location: shell\IShellFolderBand_SetBandInfoSFB.htm
tech.root: shell
ms.assetid: 6b1a219f-60a3-4073-8293-2e9e1c6459d9
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: IShellFolderBand interface [Windows Shell],SetBandInfoSFB method, IShellFolderBand.SetBandInfoSFB, IShellFolderBand::SetBandInfoSFB, SetBandInfoSFB, SetBandInfoSFB method [Windows Shell], SetBandInfoSFB method [Windows Shell],IShellFolderBand interface, _win32_IShellFolderBand_SetBandInfoSFB, shell.IShellFolderBand_SetBandInfoSFB, shlobj/IShellFolderBand::SetBandInfoSFB
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shlobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: Shell32.dll (version 5.00 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellFolderBand.SetBandInfoSFB
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellFolderBand::SetBandInfoSFB


## -description


Uses the information in a <a href="https://msdn.microsoft.com/7067f563-383d-469f-abcf-3e1ea28dc956">BANDINFOSFB</a> structure to set the band information for a <a href="https://msdn.microsoft.com/88ae35ea-6ff9-431c-848b-84fc61d3c690">IShellFolderBand</a> object.


## -parameters




### -param pbi

Type: <b>PBANDINFOSFB</b>

A pointer to a <a href="https://msdn.microsoft.com/7067f563-383d-469f-abcf-3e1ea28dc956">BANDINFOSFB</a> structure.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or an error code otherwise.




## -see-also




<a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a>



<a href="https://msdn.microsoft.com/88ae35ea-6ff9-431c-848b-84fc61d3c690">IShellFolderBand</a>
 

 

