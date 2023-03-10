---
UID: NE:fsrmenums._FsrmFileSystemPropertyId
title: FsrmFileSystemPropertyId (fsrmenums.h)
description: Defines the possible types of file system property ids.
helpviewer_keywords: ["FsrmFileSystemPropertyId","FsrmFileSystemPropertyId enumeration [File Server Resource Manager]","FsrmFileSystemPropertyId_DateCreated","FsrmFileSystemPropertyId_DateLastAccessed","FsrmFileSystemPropertyId_DateLastModified","FsrmFileSystemPropertyId_DateNow","FsrmFileSystemPropertyId_FileName","FsrmFileSystemPropertyId_Undefined","fs.fsrmfilesystempropertyid","fsrm.fsrmfilesystempropertyid","fsrmenums/FsrmFileSystemPropertyId","fsrmenums/FsrmFileSystemPropertyId_DateCreated","fsrmenums/FsrmFileSystemPropertyId_DateLastAccessed","fsrmenums/FsrmFileSystemPropertyId_DateLastModified","fsrmenums/FsrmFileSystemPropertyId_DateNow","fsrmenums/FsrmFileSystemPropertyId_FileName","fsrmenums/FsrmFileSystemPropertyId_Undefined"]
old-location: fsrm\fsrmfilesystempropertyid.htm
tech.root: fsrm
ms.assetid: 01745ffe-c50b-49a3-909f-6c32af6c656f
ms.date: 12/05/2018
ms.keywords: FsrmFileSystemPropertyId, FsrmFileSystemPropertyId enumeration [File Server Resource Manager], FsrmFileSystemPropertyId_DateCreated, FsrmFileSystemPropertyId_DateLastAccessed, FsrmFileSystemPropertyId_DateLastModified, FsrmFileSystemPropertyId_DateNow, FsrmFileSystemPropertyId_FileName, FsrmFileSystemPropertyId_Undefined, fs.fsrmfilesystempropertyid, fsrm.fsrmfilesystempropertyid, fsrmenums/FsrmFileSystemPropertyId, fsrmenums/FsrmFileSystemPropertyId_DateCreated, fsrmenums/FsrmFileSystemPropertyId_DateLastAccessed, fsrmenums/FsrmFileSystemPropertyId_DateLastModified, fsrmenums/FsrmFileSystemPropertyId_DateNow, fsrmenums/FsrmFileSystemPropertyId_FileName, fsrmenums/FsrmFileSystemPropertyId_Undefined
req.header: fsrmenums.h
req.include-header: FsrmPipeline.h, FsrmQuota.h, FsrmReports.h, FsrmScreen.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: FsrmEnums.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FsrmFileSystemPropertyId
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _FsrmFileSystemPropertyId
 - fsrmenums/_FsrmFileSystemPropertyId
 - FsrmFileSystemPropertyId
 - fsrmenums/FsrmFileSystemPropertyId
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - FsrmEnums.h
api_name:
 - FsrmFileSystemPropertyId
---

# FsrmFileSystemPropertyId enumeration


## -description

Defines the possible types of file system property ids.

## -enum-fields

### -field FsrmFileSystemPropertyId_Undefined:0

The file system property id is not used. This is the default.

### -field FsrmFileSystemPropertyId_FileName:1

The file system property id is the filename, including the extension.

### -field FsrmFileSystemPropertyId_DateCreated:2

The file system property id is the file's creation time.

### -field FsrmFileSystemPropertyId_DateLastAccessed:3

The file system property id is the file's last accessed time.

### -field FsrmFileSystemPropertyId_DateLastModified:4

The file system property id is the file's last modified time.

### -field FsrmFileSystemPropertyId_DateNow:5

The file system property id is the current time.

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrm-enumerations">FSRM Enumerations</a>



<a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfileconditionproperty-get_propertyid">IFsrmFileConditionProperty.PropertyId</a>
