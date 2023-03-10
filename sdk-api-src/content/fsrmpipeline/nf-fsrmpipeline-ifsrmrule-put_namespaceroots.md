---
UID: NF:fsrmpipeline.IFsrmRule.put_NamespaceRoots
title: IFsrmRule::put_NamespaceRoots (fsrmpipeline.h)
description: An array of directory paths that the rule is applied to when classification is run. (Put)
helpviewer_keywords: ["IFsrmRule interface [File Server Resource Manager]","NamespaceRoots property","IFsrmRule.NamespaceRoots","IFsrmRule.put_NamespaceRoots","IFsrmRule::NamespaceRoots","IFsrmRule::get_NamespaceRoots","IFsrmRule::put_NamespaceRoots","NamespaceRoots property [File Server Resource Manager]","NamespaceRoots property [File Server Resource Manager]","IFsrmRule interface","fs.ifsrmrule_namespaceroots","fsrm.ifsrmrule_namespaceroots","fsrmpipeline/IFsrmRule::NamespaceRoots","fsrmpipeline/IFsrmRule::get_NamespaceRoots","fsrmpipeline/IFsrmRule::put_NamespaceRoots","put_NamespaceRoots"]
old-location: fsrm\ifsrmrule_namespaceroots.htm
tech.root: fsrm
ms.assetid: 938ae036-fcc7-41d1-bbac-8f22b8b6333e
ms.date: 12/05/2018
ms.keywords: IFsrmRule interface [File Server Resource Manager],NamespaceRoots property, IFsrmRule.NamespaceRoots, IFsrmRule.put_NamespaceRoots, IFsrmRule::NamespaceRoots, IFsrmRule::get_NamespaceRoots, IFsrmRule::put_NamespaceRoots, NamespaceRoots property [File Server Resource Manager], NamespaceRoots property [File Server Resource Manager],IFsrmRule interface, fs.ifsrmrule_namespaceroots, fsrm.ifsrmrule_namespaceroots, fsrmpipeline/IFsrmRule::NamespaceRoots, fsrmpipeline/IFsrmRule::get_NamespaceRoots, fsrmpipeline/IFsrmRule::put_NamespaceRoots, put_NamespaceRoots
req.header: fsrmpipeline.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2
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
req.dll: SrmSvc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFsrmRule::put_NamespaceRoots
 - fsrmpipeline/IFsrmRule::put_NamespaceRoots
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SrmSvc.dll
api_name:
 - IFsrmRule.NamespaceRoots
 - IFsrmRule.get_NamespaceRoots
 - IFsrmRule.put_NamespaceRoots
---

# IFsrmRule::put_NamespaceRoots


## -description

An array of directory paths that the rule is applied to when classification is run.

This property is read/write.

## -parameters

## -remarks

All subdirectories under the specified path are also scanned (recursively).

Note that FSRM supports only NTFS file systems—you cannot specify paths on ReFS, FAT, 
    FAT32, UDF, or other non-NTFS file system.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmrule">IFsrmRule</a>
