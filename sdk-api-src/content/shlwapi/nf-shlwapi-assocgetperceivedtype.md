---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# AssocGetPerceivedType function


## -description


Retrieves a file's perceived type based on its extension.


## -parameters




### -param pszExt [in]

Type: <b>PCWSTR</b>

A pointer to a buffer that contains the file's extension. This should include the leading period, for example ".txt".


### -param ptype [out]

Type: <b><a href="https://msdn.microsoft.com/dbaf5894-1ed6-446f-ac15-12ba4c7326e7">PERCEIVED</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/dbaf5894-1ed6-446f-ac15-12ba4c7326e7">PERCEIVED</a> value that indicates the perceived type.


### -param pflag [out]

Type: <b>PERCEIVEDFLAG*</b>

A pointer to a value that indicates the source of the perceived type information. One or more of the following values.



#### PERCEIVEDFLAG_UNDEFINED (0x0000)

No perceived type was found (<a href="https://msdn.microsoft.com/dbaf5894-1ed6-446f-ac15-12ba4c7326e7">PERCEIVED_TYPE_UNSPECIFIED</a>).



#### PERCEIVEDFLAG_SOFTCODED (0x0001)

The perceived type was determined through an association in the registry.



#### PERCEIVEDFLAG_HARDCODED (0x0002)

The perceived type is inherently known to Windows.



#### PERCEIVEDFLAG_NATIVESUPPORT (0x0004)

The perceived type was determined through a codec provided with Windows.



#### PERCEIVEDFLAG_GDIPLUS (0x0010)

The perceived type is supported by the GDI+ library.



#### PERCEIVEDFLAG_WMSDK (0x0020)

The perceived type is supported by the Windows Media SDK.



#### PERCEIVEDFLAG_ZIPFOLDER (0x0040)

The perceived type is supported by Windows compressed folders.


### -param ppszType [out, optional]

Type: <b>PWSTR*</b>

If the function returns a success code, this contains the address of a pointer to a buffer that receives the perceived type string, for instance "text" or "video". This value can be <b>NULL</b>.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This function first compares the extension against a hard-coded set of extensions known to Windows. If that search fails to reveal a match, the registered associations under HKEY_CLASSES_ROOT are searched for a key that matches the extension and contains a PerceivedType value. If that value is found, the extension set is again searched for a match. If again no match is found, the perceived type is determined to be PERCEIVED_TYPE_CUSTOM. If either a key that matches the extension or a PerceivedType value is not found, the perceived type is reported as PERCEIVED_TYPE_UNSPECIFIED.



