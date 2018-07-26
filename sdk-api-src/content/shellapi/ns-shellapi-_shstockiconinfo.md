---
UID: NS:shellapi._SHSTOCKICONINFO
title: "_SHSTOCKICONINFO"
author: windows-sdk-content
description: Receives information used to retrieve a stock Shell icon. This structure is used in a call SHGetStockIconInfo.
old-location: shell\SHSTOCKICONINFO.htm
old-project: shell
ms.assetid: 4d32826a-bb40-4805-9826-801c142b8d28
ms.author: windowssdkdev
ms.date: 07/20/2018
ms.keywords: SHSTOCKICONINFO, SHSTOCKICONINFO structure [Windows Shell], _SHSTOCKICONINFO, _SHSTOCKICONINFO structure [Windows Shell], _shell_SHSTOCKICONINFO, shell.SHSTOCKICONINFO, shellapi/SHSTOCKICONINFO
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: SHSTOCKICONINFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shellapi.h
api_name:
 - _SHSTOCKICONINFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5.0
---

# _SHSTOCKICONINFO structure


## -description


Receives information used to retrieve a stock Shell icon. This structure is used in a call <a href="https://msdn.microsoft.com/c08b1a53-e67c-4ed0-a9c6-d000c448e182">SHGetStockIconInfo</a>.


## -struct-fields




### -field cbSize

Type: <b>DWORD</b>

The size of this structure, in bytes.


### -field hIcon

Type: <b>HICON</b>

When <a href="https://msdn.microsoft.com/c08b1a53-e67c-4ed0-a9c6-d000c448e182">SHGetStockIconInfo</a> is called with the SHGSI_ICON flag, this member receives a handle to the icon.


### -field iSysImageIndex

Type: <b>int</b>

When <a href="https://msdn.microsoft.com/c08b1a53-e67c-4ed0-a9c6-d000c448e182">SHGetStockIconInfo</a> is called with the SHGSI_SYSICONINDEX flag, this member receives the index of the image in the system icon cache.


### -field iIcon

Type: <b>int</b>

When <a href="https://msdn.microsoft.com/c08b1a53-e67c-4ed0-a9c6-d000c448e182">SHGetStockIconInfo</a> is called with the SHGSI_ICONLOCATION flag, this member receives the index of the icon in the resource whose path is received in <b>szPath</b>.


### -field szPath

Type: <b>WCHAR[MAX_PATH]</b>

When <a href="https://msdn.microsoft.com/c08b1a53-e67c-4ed0-a9c6-d000c448e182">SHGetStockIconInfo</a> is called with the SHGSI_ICONLOCATION flag, this member receives the path of the resource that contains the icon. The index of the icon within the resource is received in <b>iIcon</b>.


## -see-also




<a href="https://msdn.microsoft.com/c08b1a53-e67c-4ed0-a9c6-d000c448e182">SHGetStockIconInfo</a>
 

 

