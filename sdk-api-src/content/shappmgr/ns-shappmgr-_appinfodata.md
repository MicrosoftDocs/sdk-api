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

# _AppInfoData structure


## -description


Provides information about a published application to the Add/Remove Programs Control Panel utility.


## -struct-fields




### -field cbSize

Type: <b>DWORD</b>

A value of type <b>DWORD</b> that specifies the size of the <b>APPINFODATA</b> data structure. This field is set by the Add/Remove Program executable code.


### -field dwMask

Type: <b>DWORD</b>

A value of type <b>DWORD</b> that specifies the bitmask that indicates which items in the structure are desired or valid. Implementations of <a href="https://msdn.microsoft.com/8842c12e-2b59-49d6-8140-5a402509a0dd">GetAppInfo</a> should inspect this value for bits that are set and attempt to provide values corresponding to those bits. Implementations should also return with bits set for only those members that are being returned.


### -field pszDisplayName

Type: <b>LPWSTR</b>

A pointer to a string that contains the application display name. Memory for this string must be allocated using <a href="https://msdn.microsoft.com/c4cb588d-9482-4f90-a92e-75b604540d5c">CoTaskMemAlloc</a> and freed using <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>.


### -field pszVersion

Type: <b>LPWSTR</b>

Not applicable to published applications.


### -field pszPublisher

 


### -field pszProductID

Type: <b>LPWSTR</b>

Not applicable to published applications.


### -field pszRegisteredOwner

Type: <b>LPWSTR</b>

Not applicable to published applications.


### -field pszRegisteredCompany

Type: <b>LPWSTR</b>

Not applicable to published applications.


### -field pszLanguage

Type: <b>LPWSTR</b>

Not applicable to published applications.

Type: <b>LPWSTR</b>

Not applicable to published applications.


### -field pszSupportUrl

Type: <b>LPWSTR</b>

A URL to support information. This string is displayed as a link with the application name in Control Panel Add/Remove Programs. Memory for this string must be allocated using <a href="https://msdn.microsoft.com/c4cb588d-9482-4f90-a92e-75b604540d5c">CoTaskMemAlloc</a> and freed using <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>.


### -field pszSupportTelephone

Type: <b>LPWSTR</b>

Not applicable to published applications.


### -field pszHelpLink

Type: <b>LPWSTR</b>

Not applicable to published applications.


### -field pszInstallLocation

Type: <b>LPWSTR</b>

Not applicable to published applications.


### -field pszInstallSource

Type: <b>LPWSTR</b>

Not applicable to published applications.


### -field pszInstallDate

Type: <b>LPWSTR</b>

Not applicable to published applications.


### -field pszContact

Type: <b>LPWSTR</b>

Not applicable to published applications.


### -field pszComments

Type: <b>LPWSTR</b>

Not applicable to published applications.


### -field pszImage

Type: <b>LPWSTR</b>

Not applicable to published applications.


### -field pszReadmeUrl

Type: <b>LPWSTR</b>

Not applicable to published applications.


### -field pszUpdateInfoUrl

Type: <b>LPWSTR</b>

Not applicable to published applications.


## -see-also




<a href="https://msdn.microsoft.com/5391444a-53b6-48c9-9a94-d045b3f97182">IAppPublisher</a>



<a href="https://msdn.microsoft.com/4ffcc30a-cf07-45e7-b9a5-342fe2b553c8">IPublishedApp::GetPublishedAppInfo</a>
 

 

