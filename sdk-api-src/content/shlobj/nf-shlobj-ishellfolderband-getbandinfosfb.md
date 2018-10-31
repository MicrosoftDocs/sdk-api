---
UID: NF:shlobj.IShellFolderBand.GetBandInfoSFB
title: IShellFolderBand::GetBandInfoSFB
author: windows-sdk-content
description: Gets information concerning an IShellFolderBand object and places it in a BANDINFOSFB structure.
old-location: shell\IShellFolderBand_GetBandInfoSFB.htm
tech.root: shell
ms.assetid: 7a42ba12-987a-4b43-9d95-085a5e896245
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: GetBandInfoSFB, GetBandInfoSFB method [Windows Shell], GetBandInfoSFB method [Windows Shell],IShellFolderBand interface, IShellFolderBand interface [Windows Shell],GetBandInfoSFB method, IShellFolderBand.GetBandInfoSFB, IShellFolderBand::GetBandInfoSFB, _win32_IShellFolderBand_GetBandInfoSFB, shell.IShellFolderBand_GetBandInfoSFB, shlobj/IShellFolderBand::GetBandInfoSFB
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
 - IShellFolderBand.GetBandInfoSFB
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellFolderBand::GetBandInfoSFB


## -description


Gets information concerning an <a href="https://msdn.microsoft.com/88ae35ea-6ff9-431c-848b-84fc61d3c690">IShellFolderBand</a> object and places it in a <a href="https://msdn.microsoft.com/7067f563-383d-469f-abcf-3e1ea28dc956">BANDINFOSFB</a> structure.


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
 

 

