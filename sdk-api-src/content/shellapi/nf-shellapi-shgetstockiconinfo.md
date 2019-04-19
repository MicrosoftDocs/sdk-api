---
UID: NF:shellapi.SHGetStockIconInfo
title: SHGetStockIconInfo function (shellapi.h)
author: windows-sdk-content
description: Retrieves information about system-defined Shell icons.
old-location: shell\SHGetStockIconInfo.htm
tech.root: shell
ms.assetid: c08b1a53-e67c-4ed0-a9c6-d000c448e182
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SHGSI_ICON, SHGSI_ICONLOCATION, SHGSI_LARGEICON, SHGSI_LINKOVERLAY, SHGSI_SELECTED, SHGSI_SHELLICONSIZE, SHGSI_SMALLICON, SHGSI_SYSICONINDEX, SHGetStockIconInfo, SHGetStockIconInfo function [Windows Shell], _shell_SHGetStockIconInfo, shell.SHGetStockIconInfo, shellapi/SHGetStockIconInfo
ms.topic: function
req.header: shellapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: Shell32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
 - ext-ms-win-shell-shell32-l1-2-1.dll
 - Ext-MS-Win-Shell-Shell32-L1-2-2.dll
api_name:
 - SHGetStockIconInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SHGetStockIconInfo function


## -description


Retrieves information about system-defined Shell icons.


## -parameters




### -param siid

Type: <b><a href="https://msdn.microsoft.com/37da5555-3626-465e-b834-3a28b75495c4">SHSTOCKICONID</a></b>

One of the values from the <a href="https://msdn.microsoft.com/37da5555-3626-465e-b834-3a28b75495c4">SHSTOCKICONID</a> enumeration that specifies which icon should be retrieved.


### -param uFlags

Type: <b>UINT</b>

A combination of zero or more of the following flags that specify which information is requested.



#### SHGSI_ICONLOCATION

The <b>szPath</b> and <b>iIcon</b> members of the <a href="https://msdn.microsoft.com/4d32826a-bb40-4805-9826-801c142b8d28">SHSTOCKICONINFO</a> structure receive the path and icon index of the requested icon, in a format suitable for passing to the <a href="https://msdn.microsoft.com/a0314423-79d6-416e-8be0-be946477da3e">ExtractIcon</a> function. The numerical value of this flag is zero, so you always get the icon location regardless of other flags.



#### SHGSI_ICON

The <b>hIcon</b> member of the <a href="https://msdn.microsoft.com/4d32826a-bb40-4805-9826-801c142b8d28">SHSTOCKICONINFO</a> structure receives a handle to the specified icon.



#### SHGSI_SYSICONINDEX

The <b>iSysImageImage</b> member of the <a href="https://msdn.microsoft.com/4d32826a-bb40-4805-9826-801c142b8d28">SHSTOCKICONINFO</a> structure receives the index of the specified icon in the system imagelist.



#### SHGSI_LINKOVERLAY

Modifies the SHGSI_ICON value by causing the function to add the link overlay to the file's icon.



#### SHGSI_SELECTED

Modifies the SHGSI_ICON value by causing the function to blend the icon with the system highlight color.



#### SHGSI_LARGEICON

Modifies the SHGSI_ICON value by causing the function to retrieve the large version of the icon, as specified by the SM_CXICON and SM_CYICON system metrics.



#### SHGSI_SMALLICON

Modifies the SHGSI_ICON value by causing the function to retrieve the small version of the icon, as specified by the SM_CXSMICON and SM_CYSMICON system metrics.



#### SHGSI_SHELLICONSIZE

Modifies the SHGSI_LARGEICON or SHGSI_SMALLICON values by causing the function to retrieve the Shell-sized icons rather than the sizes specified by the system metrics.


### -param psii [in, out]

Type: <b><a href="https://msdn.microsoft.com/4d32826a-bb40-4805-9826-801c142b8d28">SHSTOCKICONINFO</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/4d32826a-bb40-4805-9826-801c142b8d28">SHSTOCKICONINFO</a> structure. When this function is called, the <b>cbSize</b> member of this structure needs to be set to the size of the <b>SHSTOCKICONINFO</b> structure. When this function returns, contains a pointer to a <b>SHSTOCKICONINFO</b> structure that contains the requested information.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If this function returns an icon handle in the <b>hIcon</b> member of the <a href="https://msdn.microsoft.com/4d32826a-bb40-4805-9826-801c142b8d28">SHSTOCKICONINFO</a>  structure pointed to by <i>psii</i>, you are responsible for freeing the icon with <a href="https://msdn.microsoft.com/en-us/library/ms648063(v=VS.85).aspx">DestroyIcon</a> when you no longer need it.



