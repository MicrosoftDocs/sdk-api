---
UID: NS:winnls._nlsversioninfoex
title: NLSVERSIONINFOEX
author: windows-sdk-content
description: Contains version information about an NLS capability.
old-location: intl\nlsversioninfoex.htm
tech.root: Intl
ms.assetid: 97f637df-3e0e-4349-a617-96b7c640b19d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPNLSVERSIONINFOEX, LPNLSVERSIONINFOEX, LPNLSVERSIONINFOEX structure pointer [Internationalization for Windows Applications], NLSVERSIONINFOEX, NLSVERSIONINFOEX structure [Internationalization for Windows Applications], _win32_NLSVERSIONINFOEX_str, intl.nlsversioninfoex, winnls/LPNLSVERSIONINFOEX, winnls/NLSVERSIONINFOEX"
ms.topic: struct
req.header: winnls.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - Winnls.h
api_name:
 - NLSVERSIONINFOEX
product: Windows
targetos: Windows
req.typenames: NLSVERSIONINFOEX, *LPNLSVERSIONINFOEX
req.redist: 
---

# NLSVERSIONINFOEX structure


## -description



Contains version information about an NLS capability.




## -struct-fields




### -field dwNLSVersionInfoSize

Size, in bytes, of the structure.


### -field dwNLSVersion

Version. This value is used to track changes and additions to the set of code points that have the indicated capability for a particular locale. The value is locale-specific, and increments when the capability changes. For example, using the COMPARE_STRING capability defined by the <a href="https://msdn.microsoft.com/c34eb904-e264-4f7d-ac7f-4ec8cfc588b6">SYSNLS_FUNCTION</a> enumeration, the version changes if sorting weights are assigned to code points that previously had no weights defined for the locale.


### -field dwDefinedVersion

Defined version. This value is used to track changes in the repertoire of Unicode code points. The value increments when the Unicode repertoire is extended, for example, if more characters are defined.

<b>Starting with Windows 8:</b> Deprecated. Use <b>dwNLSVersion</b> instead.


### -field dwEffectiveId

Identifier of the sort order used for the input locale for the represented version. For example, for a custom locale en-Mine that uses 0409 for a sort order identifier, this member contains "0409". If this member specifies a "real" sort, <b>guidCustomVersion</b> is set to an empty GUID.

<b>Starting with Windows 8:</b> Deprecated. Use <b>guidCustomVersion</b> instead.


### -field guidCustomVersion

Unique GUID for the behavior of a custom sort used by the locale for the represented version.


## -remarks



The <b>dwNLSVersion</b> and <b>dwDefinedVersion</b> members are completely independent. Although each member is defined for a single DWORD, actually each is composed of a major version and a minor version. See <a href="https://msdn.microsoft.com/c8fc32bd-02bd-4a40-a836-d9ad9f69c209">Handling Sorting in Your Applications</a> for more information.




## -see-also




<a href="https://msdn.microsoft.com/255e6774-eb70-41db-a372-8796166ee8d6">GetNLSVersionEx</a>



<a href="https://msdn.microsoft.com/c8fc32bd-02bd-4a40-a836-d9ad9f69c209">Handling Sorting in Your Applications</a>



<a href="https://msdn.microsoft.com/0beb0470-ecdc-4a24-b28c-0738e1df9d49">IsNLSDefinedString</a>



<a href="https://msdn.microsoft.com/75382149-7d4e-4b3e-929e-ee39bf666110">National Language Support Structures</a>
 

 

