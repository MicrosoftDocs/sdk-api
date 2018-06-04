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

# tagTYSPEC enumeration


## -description


Specifies a mapping for a class ID.


## -enum-fields




### -field TYSPEC_CLSID

A CLSID.


### -field TYSPEC_FILEEXT

A file name extension.


### -field TYSPEC_MIMETYPE

A MIME type.


### -field TYSPEC_FILENAME

A file name.


### -field TYSPEC_PROGID

A PROGID.


### -field TYSPEC_PACKAGENAME

A package name.


### -field TYSPEC_OBJECTID

An object ID.


## -remarks



The TYSPEC enumeration and uCLSSPEC union provide mappings to a class ID. Note that TYSPEC_CLSID is the only supported value.

<pre class="syntax" xml:space="preserve"><code>    typedef union switch(DWORD tyspec)
        {
        case TYSPEC_CLSID:
            CLSID   clsid;
        case TYSPEC_FILEEXT:
            LPOLESTR pFileExt;
        case TYSPEC_MIMETYPE:
            LPOLESTR pMimeType;
        case TYSPEC_PROGID:
            LPOLESTR pProgId;
        case TYSPEC_FILENAME:
            LPOLESTR pFileName;
        case TYSPEC_PACKAGENAME:
            struct {
            LPOLESTR pPackageName;
            GUID     PolicyId;
            } ByName;
        case TYSPEC_OBJECTID:
            struct {
            GUID     ObjectId;
            GUID     PolicyId;
            } ByObjectId;
    } uCLSSPEC;</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/9486ef2d-51a1-41b4-85e5-427af9a98cec">CoInstall</a>
 

 

