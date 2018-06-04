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

# SHFOLDERCUSTOMSETTINGS structure


## -description


Holds custom folder settings. This structure is used with the <a href="https://msdn.microsoft.com/38b78a4b-ba68-4dff-812d-d4c7421eb202">SHGetSetFolderCustomSettings</a> function.


## -struct-fields




### -field dwSize

Type: <b>DWORD</b>

The size of the structure, in bytes.


### -field dwMask

Type: <b>DWORD</b>

A <b>DWORD</b> value specifying which folder attributes to read or write from this structure. Use one or more of the following values to indicate which structure members are valid:



#### FCSM_VIEWID

<b>Deprecated</b>. <b>pvid</b> contains the folder's GUID.



#### FCSM_WEBVIEWTEMPLATE

<b>Deprecated</b>. <b>pszWebViewTemplate</b> contains a pointer to a buffer containing the path to the folder's WebView template.



#### FCSM_INFOTIP

<b>pszInfoTip</b> contains a pointer to a buffer containing the folder's info tip.



#### FCSM_CLSID

<b>pclsid</b> contains the folder's CLSID.



#### FCSM_ICONFILE

<b>pszIconFile</b> contains the path to the file containing the folder's icon.



#### FCSM_LOGO

<b>pszLogo</b> contains the path to the file containing the folder's thumbnail icon.



#### FCSM_FLAGS

Not used.


### -field pvid

Type: <b>SHELLVIEWID*</b>

The folder's GUID.


### -field pszWebViewTemplate

Type: <b>LPTSTR</b>

A pointer to a null-terminated string containing the path to the folder's <a href="https://msdn.microsoft.com/a894df21-bcc6-4760-b7d7-9bf95a0dba7f">WebView template</a>.


### -field cchWebViewTemplate

Type: <b>DWORD</b>

If the <a href="https://msdn.microsoft.com/38b78a4b-ba68-4dff-812d-d4c7421eb202">SHGetSetFolderCustomSettings</a> parameter <i>dwReadWrite</i> is <b>FCS_READ</b>, this is the size of the <b>pszWebViewTemplate</b> buffer, in characters. If not, this is the number of characters to write from that buffer. Set this parameter to 0 to write the entire string.


### -field pszWebViewTemplateVersion

Type: <b>LPTSTR</b>

A pointer to a null-terminated buffer containing the WebView template version.


### -field pszInfoTip

Type: <b>LPTSTR</b>

A pointer to a null-terminated buffer containing the text of the folder's infotip.


### -field cchInfoTip

Type: <b>DWORD</b>

If the <a href="https://msdn.microsoft.com/38b78a4b-ba68-4dff-812d-d4c7421eb202">SHGetSetFolderCustomSettings</a> parameter <i>dwReadWrite</i> is <b>FCS_READ</b>, this is the size of the <b>pszInfoTip</b> buffer, in characters. If not, this is the number of characters to write from that buffer. Set this parameter to 0 to write the entire string.


### -field pclsid

Type: <b>CLSID*</b>

A pointer to a CLSID used to identify the folder in the Windows registry. Further folder information is stored in the registry under that CLSID entry.


### -field dwFlags

Type: <b>DWORD</b>

Not used.


### -field pszIconFile

Type: <b>LPTSTR</b>

A pointer to a null-terminated buffer containing the path to file containing the folder's icon.


### -field cchIconFile

Type: <b>DWORD</b>

If the <a href="https://msdn.microsoft.com/38b78a4b-ba68-4dff-812d-d4c7421eb202">SHGetSetFolderCustomSettings</a> parameter <i>dwReadWrite</i> is <b>FCS_READ</b>, this is the size of the <b>pszIconFile</b> buffer, in characters. If not, this is the number of characters to write from that buffer. Set this parameter to 0 to write the entire string.


### -field iIconIndex

Type: <b>int</b>

The index of the icon within the file named in <b>pszIconFile</b>.


### -field pszLogo

Type: <b>LPTSTR</b>

A pointer to a null-terminated buffer containing the path to the file containing the folder's logo image. This is the image used in thumbnail views.


### -field cchLogo

Type: <b>DWORD</b>

If the <a href="https://msdn.microsoft.com/38b78a4b-ba68-4dff-812d-d4c7421eb202">SHGetSetFolderCustomSettings</a> parameter <i>dwReadWrite</i> is <b>FCS_READ</b>, this is the size of the <b>pszLogo</b> buffer, in characters. If not, this is the number of characters to write from that buffer. Set this parameter to 0 to write the entire string.


## -remarks



In Windows XP Service Pack 2 (SP2) and earlier versions, this structure supported both ANSI and Unicode strings. In Windows Vista and later versions, only Unicode strings are supported.



