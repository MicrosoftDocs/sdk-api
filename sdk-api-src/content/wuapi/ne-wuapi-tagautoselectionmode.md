---
UID: NE:wuapi.tagAutoSelectionMode
title: tagAutoSelectionMode
author: windows-sdk-content
description: Defines the types of logic that is used to determine whether a particular update will be automatically selected when the user views available updates in the Windows Update user interface.
old-location: wua\autoselectionmode.htm
tech.root: Wua_Sdk
ms.assetid: 847fd8a3-eb00-43f7-a89f-579cd79d0620
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: AutoSelectionMode, AutoSelectionMode enumeration [Windows Update Agent], asAlwaysAutoSelect, asAutoSelectIfDownloaded, asLetWindowsUpdateDecide, asNeverAutoSelect, tagAutoSelectionMode, wua.autoselectionmode, wuapi/AutoSelectionMode, wuapi/asAlwaysAutoSelect, wuapi/asAutoSelectIfDownloaded, wuapi/asLetWindowsUpdateDecide, wuapi/asNeverAutoSelect
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: wuapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wuapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wuapi.h
api_name:
 - AutoSelectionMode
product: Windows
targetos: Windows
req.typenames: AutoSelectionMode
req.redist: 
---

# tagAutoSelectionMode enumeration


## -description


Defines  the types of logic that is used to determine whether a particular update will be automatically selected when the user views  available updates in the Windows Update user interface.


## -enum-fields




### -field asLetWindowsUpdateDecide

Use the standard logic. The update will be automatically selected if it is important, or if it is recommended and Windows Update has been configured to treat recommended updates as important. Otherwise, the update will not be automatically selected.


### -field asAutoSelectIfDownloaded

The update will be automatically selected only if it has been completely downloaded.


### -field asNeverAutoSelect

The update will never be automatically selected.


### -field asAlwaysAutoSelect

The update will always be automatically selected.


## -remarks



In versions of the Windows Update Agent (WUA) in which <a href="https://msdn.microsoft.com/ff290e39-7d7c-42da-a522-ba9e672721b8">IUpdate5</a> is not available, all updates are processed by using the standard logic.



