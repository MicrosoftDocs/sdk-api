---
UID: NF:comppkgsup.GetMediaComponentPackageInfo
title: GetMediaComponentPackageInfo function (comppkgsup.h)
author: windows-sdk-content
description: Returns a list of properties for all media codecs installed on the system that meet the specified requirements.
old-location: winprog\getmediacomponentpackageinfo.htm
tech.root: DevNotes
ms.assetid: EDBC9F34-62C3-4256-9AEC-9A743608B5B7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetMediaComponentPackageInfo, GetMediaComponentPackageInfo function [Windows API], comppkgsup/GetMediaComponentPackageInfo, winprog.getmediacomponentpackageinfo
ms.topic: function
f1_keywords: 
 - "comppkgsup/GetMediaComponentPackageInfo"
req.header: comppkgsup.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Comppkgsup.lib
req.dll: CompPkgSup.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - CompPkgSup.dll
api_name:
 - GetMediaComponentPackageInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetMediaComponentPackageInfo function


## -description


Returns a list of properties for all media codecs installed on the system that meet the specified requirements.


## -parameters




### -param trustedOnly [in]

True if the query should only return properties for packages that run in the app's process space; false if the query should include packages that run in  a separate app service.


### -param category [in]

A string that specifies the category of packages that should be included in the results.


### -param codecPropertiesVector [out]

A list of <a href="https://docs.microsoft.com/en-us/uwp/api/windows.foundation.collections.ipropertyset">IPropertySet</a> objects representing the properties of the installed media component packages that meet the specified criteria.


## -returns



Returns S_OK on successful completion.



