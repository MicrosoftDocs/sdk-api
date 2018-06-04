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

# _nlsversioninfoex structure


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
 

 

