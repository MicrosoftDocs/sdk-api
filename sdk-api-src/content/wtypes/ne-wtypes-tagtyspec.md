---
UID: NE:wtypes.tagTYSPEC
title: tagTYSPEC
author: windows-sdk-content
description: Specifies a mapping for a class ID.
old-location: com\tyspec.htm
old-project: com
ms.assetid: f2972300-5a95-43e3-b2d1-cd8f30d14d1d
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: TYSPEC, TYSPEC enumeration [COM], TYSPEC_CLSID, TYSPEC_FILEEXT, TYSPEC_FILENAME, TYSPEC_MIMETYPE, TYSPEC_OBJECTID, TYSPEC_PACKAGENAME, TYSPEC_PROGID, _com_TYSPEC, com.tyspec, tagTYSPEC, wtypes/TYSPEC, wtypes/TYSPEC_CLSID, wtypes/TYSPEC_FILEEXT, wtypes/TYSPEC_FILENAME, wtypes/TYSPEC_MIMETYPE, wtypes/TYSPEC_OBJECTID, wtypes/TYSPEC_PACKAGENAME, wtypes/TYSPEC_PROGID
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: wtypes.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WTypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TYSPEC
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WTypes.h
api_name:
 - TYSPEC
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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
 

 

