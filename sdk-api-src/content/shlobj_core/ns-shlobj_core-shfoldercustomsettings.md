---
UID: NS:shlobj_core.SHFOLDERCUSTOMSETTINGS
title: SHFOLDERCUSTOMSETTINGS (shlobj_core.h)
description: Holds custom folder settings. This structure is used with the SHGetSetFolderCustomSettings function.
helpviewer_keywords: ["*LPSHFOLDERCUSTOMSETTINGS","FCSM_CLSID","FCSM_FLAGS","FCSM_ICONFILE","FCSM_INFOTIP","FCSM_LOGO","FCSM_VIEWID","FCSM_WEBVIEWTEMPLATE","LPSHFOLDERCUSTOMSETTINGS","LPSHFOLDERCUSTOMSETTINGS structure pointer [Windows Shell]","SHFOLDERCUSTOMSETTINGS","SHFOLDERCUSTOMSETTINGS structure [Windows Shell]","SHFOLDERCUSTOMSETTINGSA","SHFOLDERCUSTOMSETTINGSW","_win32_SHFOLDERCUSTOMSETTINGS","shell.SHFOLDERCUSTOMSETTINGS","shlobj_core/LPSHFOLDERCUSTOMSETTINGS","shlobj_core/SHFOLDERCUSTOMSETTINGS","shlobj_core/SHFOLDERCUSTOMSETTINGSA","shlobj_core/SHFOLDERCUSTOMSETTINGSW"]
old-location: shell\SHFOLDERCUSTOMSETTINGS.htm
tech.root: shell
ms.assetid: a6357372-80ef-4719-b53f-87eb3fdc1b0d
ms.date: 12/05/2018
ms.keywords: '*LPSHFOLDERCUSTOMSETTINGS, FCSM_CLSID, FCSM_FLAGS, FCSM_ICONFILE, FCSM_INFOTIP, FCSM_LOGO, FCSM_VIEWID, FCSM_WEBVIEWTEMPLATE, LPSHFOLDERCUSTOMSETTINGS, LPSHFOLDERCUSTOMSETTINGS structure pointer [Windows Shell], SHFOLDERCUSTOMSETTINGS, SHFOLDERCUSTOMSETTINGS structure [Windows Shell], SHFOLDERCUSTOMSETTINGSA, SHFOLDERCUSTOMSETTINGSW, _win32_SHFOLDERCUSTOMSETTINGS, shell.SHFOLDERCUSTOMSETTINGS, shlobj_core/LPSHFOLDERCUSTOMSETTINGS, shlobj_core/SHFOLDERCUSTOMSETTINGS, shlobj_core/SHFOLDERCUSTOMSETTINGSA, shlobj_core/SHFOLDERCUSTOMSETTINGSW'
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SHFOLDERCUSTOMSETTINGSW (Unicode) and SHFOLDERCUSTOMSETTINGSA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SHFOLDERCUSTOMSETTINGS, *LPSHFOLDERCUSTOMSETTINGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LPSHFOLDERCUSTOMSETTINGS
 - shlobj_core/LPSHFOLDERCUSTOMSETTINGS
 - SHFOLDERCUSTOMSETTINGS
 - shlobj_core/SHFOLDERCUSTOMSETTINGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shlobj_core.h
api_name:
 - SHFOLDERCUSTOMSETTINGS
 - SHFOLDERCUSTOMSETTINGSA
 - SHFOLDERCUSTOMSETTINGSW
---

# SHFOLDERCUSTOMSETTINGS structure


## -description

Holds custom folder settings. This structure is used with the <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetsetfoldercustomsettings">SHGetSetFolderCustomSettings</a> function.

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

A pointer to a null-terminated string containing the path to the folder's <a href="/windows/desktop/lwef/web-view">WebView template</a>.

### -field cchWebViewTemplate

Type: <b>DWORD</b>

If the <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetsetfoldercustomsettings">SHGetSetFolderCustomSettings</a> parameter <i>dwReadWrite</i> is <b>FCS_READ</b>, this is the size of the <b>pszWebViewTemplate</b> buffer, in characters. If not, this is the number of characters to write from that buffer. Set this parameter to 0 to write the entire string.

### -field pszWebViewTemplateVersion

Type: <b>LPTSTR</b>

A pointer to a null-terminated buffer containing the WebView template version.

### -field pszInfoTip

Type: <b>LPTSTR</b>

A pointer to a null-terminated buffer containing the text of the folder's infotip.

### -field cchInfoTip

Type: <b>DWORD</b>

If the <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetsetfoldercustomsettings">SHGetSetFolderCustomSettings</a> parameter <i>dwReadWrite</i> is <b>FCS_READ</b>, this is the size of the <b>pszInfoTip</b> buffer, in characters. If not, this is the number of characters to write from that buffer. Set this parameter to 0 to write the entire string.

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

If the <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetsetfoldercustomsettings">SHGetSetFolderCustomSettings</a> parameter <i>dwReadWrite</i> is <b>FCS_READ</b>, this is the size of the <b>pszIconFile</b> buffer, in characters. If not, this is the number of characters to write from that buffer. Set this parameter to 0 to write the entire string.

### -field iIconIndex

Type: <b>int</b>

The index of the icon within the file named in <b>pszIconFile</b>.

### -field pszLogo

Type: <b>LPTSTR</b>

A pointer to a null-terminated buffer containing the path to the file containing the folder's logo image. This is the image used in thumbnail views.

### -field cchLogo

Type: <b>DWORD</b>

If the <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetsetfoldercustomsettings">SHGetSetFolderCustomSettings</a> parameter <i>dwReadWrite</i> is <b>FCS_READ</b>, this is the size of the <b>pszLogo</b> buffer, in characters. If not, this is the number of characters to write from that buffer. Set this parameter to 0 to write the entire string.

## -remarks

In Windows XP Service Pack 2 (SP2) and earlier versions, this structure supported both ANSI and Unicode strings. In Windows Vista and later versions, only Unicode strings are supported.

