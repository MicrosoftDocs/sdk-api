---
UID: NE:minwinbase._GET_FILEEX_INFO_LEVELS
title: "_GET_FILEEX_INFO_LEVELS"
author: windows-sdk-content
description: Defines values that are used with the GetFileAttributesEx and GetFileAttributesTransacted functions to specify the information level of the returned data.
old-location: fs\get_fileex_info_levels.htm
tech.root: fileio
ms.assetid: 1004ab99-9c08-4ed4-ba5f-d72f1b44a415
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: GET_FILEEX_INFO_LEVELS, GET_FILEEX_INFO_LEVELS enumeration [Files], GetFileExInfoStandard, GetFileExMaxInfoLevel, _GET_FILEEX_INFO_LEVELS, fs.get_fileex_info_levels, winbase/GET_FILEEX_INFO_LEVELS, winbase/GetFileExInfoStandard, winbase/GetFileExMaxInfoLevel
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: minwinbase.h
req.include-header: Minwinbase.h, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinBase.h
api_name:
 - GET_FILEEX_INFO_LEVELS
product: Windows
targetos: Windows
req.typenames: GET_FILEEX_INFO_LEVELS
req.redist: 
---

# _GET_FILEEX_INFO_LEVELS enumeration


## -description


Defines values that are used with the 
    <a href="https://msdn.microsoft.com/e5d84000-17c1-4517-97a7-6bd240d73814">GetFileAttributesEx</a> and 
    <a href="https://msdn.microsoft.com/dd1435da-93e5-440a-913a-9e40e39b4a01">GetFileAttributesTransacted</a> functions to 
    specify the information level of the returned data.


## -enum-fields




### -field GetFileExInfoStandard

The <a href="https://msdn.microsoft.com/e5d84000-17c1-4517-97a7-6bd240d73814">GetFileAttributesEx</a> or 
      <a href="https://msdn.microsoft.com/dd1435da-93e5-440a-913a-9e40e39b4a01">GetFileAttributesTransacted</a> function 
      retrieves a standard set of attribute information. The data is returned in a 
      <a href="https://msdn.microsoft.com/e1a7fb5c-2d69-40e3-b9d8-b583a03d828a">WIN32_FILE_ATTRIBUTE_DATA</a> 
      structure.


### -field GetFileExMaxInfoLevel

One greater than the maximum value. Valid values for this enumeration will be less than this value.


## -see-also




<a href="https://msdn.microsoft.com/14b1cfff-5e47-4309-8e62-fb5c8da9ce97">File Management Enumerations</a>



<a href="https://msdn.microsoft.com/e5d84000-17c1-4517-97a7-6bd240d73814">GetFileAttributesEx</a>



<a href="https://msdn.microsoft.com/dd1435da-93e5-440a-913a-9e40e39b4a01">GetFileAttributesTransacted</a>



<a href="https://msdn.microsoft.com/e1a7fb5c-2d69-40e3-b9d8-b583a03d828a">WIN32_FILE_ATTRIBUTE_DATA</a>
 

 

