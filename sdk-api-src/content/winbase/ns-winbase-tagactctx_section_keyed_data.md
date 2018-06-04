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

# tagACTCTX_SECTION_KEYED_DATA structure


## -description


The 
<b>ACTCTX_SECTION_KEYED_DATA</b> structure is used by the 
<a href="https://msdn.microsoft.com/d3f0b057-44ec-47ec-a0aa-69f3540b8900">FindActCtxSectionString</a> and 
<a href="https://msdn.microsoft.com/3889505c-29a0-49dd-aca8-a26417b25a94">FindActCtxSectionGuid</a> functions to return the activation context information along with either the GUID or 32-bit integer-tagged activation context section.


## -struct-fields




### -field cbSize

The size, in bytes, of the activation context keyed data structure.


### -field ulDataFormatVersion

Number that indicates the format of the data in the section where the key was found. Clients should verify that the data format version is as expected rather than trying to interpret the values of unfamiliar data formats. This number is only changed when major non-backward-compatible changes to the section data formats need to be made. The current format version is 1.


### -field lpData

Pointer to the redirection data found associated with the section identifier and key.


### -field ulLength

Number of bytes in the structure referred to by <b>lpData</b>. Note that the data structures  grow over time; do not access members in the instance data that extend beyond <b>ulLength</b>.


### -field lpSectionGlobalData

Returned pointer to a section-specific data structure which is global to the activation context section where the key was found. Its interpretation depends on the section identifier requested.


### -field ulSectionGlobalDataLength

Number of bytes in the section global data block referred to by <b>lpSectionGlobalData</b>. 




Note that the data structures  grow over time and you may receive an old format activation context data block; do not access members in the section global data that extend beyond <b>ulSectionGlobalDataLength</b>.


### -field lpSectionBase

Pointer to the base of the section where the key was found. Some instance data contains offsets relative to the section base address, in which case this pointer value is used.


### -field ulSectionTotalLength

Number of bytes for the entire section starting at <b>lpSectionBase</b>. May be used to verify that offset/length pairs, which are specified as relative to the section base are wholly contained in the section.


### -field hActCtx

Handle to the activation context where the key was found. First, the active activation context for the thread is searched, followed by the process-default activation context and then the system-compatible-default-activation context. This member indicates which activation context contained the section and key requested. This is only returned if the FIND_ACTCTX_SECTION_KEY_RETURN_HACTCTX flag is passed. 




Note that when this is returned, the caller must call 
<a href="https://msdn.microsoft.com/aaf58969-06b7-4981-83af-651252339186">ReleaseActCtx</a>() on the activation context handle returned to release system resources when all other references to the activation context have been released.


### -field ulAssemblyRosterIndex

Cardinal number of the assembly in the activation context that provided the redirection information found. This value can be presented to <a href="https://msdn.microsoft.com/7d45f63f-0baf-4236-b245-d36f9eb32e8c">QueryActCtxW</a> for more information about the contributing assembly.


### -field ulFlags

 


### -field AssemblyMetadata

 




## -remarks



Callers should initialize the 
<b>ACTCTX_SECTION_KEYED_DATA</b> structure as such:

"ACTCTX_SECTION_KEYED_DATA askd = { sizeof(askd) };"

which  initializes all members to zero/null except the size field which is set correctly.




## -see-also




<a href="https://msdn.microsoft.com/b6f97f25-1834-44f7-86b7-33339481ba60">ACTCTX</a>



<a href="https://msdn.microsoft.com/3889505c-29a0-49dd-aca8-a26417b25a94">FindActCtxSectionGuid</a>



<a href="https://msdn.microsoft.com/d3f0b057-44ec-47ec-a0aa-69f3540b8900">FindActCtxSectionString</a>
 

 

