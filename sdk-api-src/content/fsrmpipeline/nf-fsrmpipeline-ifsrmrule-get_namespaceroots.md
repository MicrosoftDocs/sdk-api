---
UID: NF:fsrmpipeline.IFsrmRule.get_NamespaceRoots
title: IFsrmRule::get_NamespaceRoots
author: windows-sdk-content
description: An array of directory paths that the rule is applied to when classification is run.
old-location: fsrm\ifsrmrule_namespaceroots.htm
old-project: Fsrm
ms.assetid: 938ae036-fcc7-41d1-bbac-8f22b8b6333e
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: IFsrmRule interface [File Server Resource Manager],NamespaceRoots property, IFsrmRule.NamespaceRoots, IFsrmRule.get_NamespaceRoots, IFsrmRule::NamespaceRoots, IFsrmRule::get_NamespaceRoots, IFsrmRule::put_NamespaceRoots, NamespaceRoots property [File Server Resource Manager], NamespaceRoots property [File Server Resource Manager],IFsrmRule interface, fs.ifsrmrule_namespaceroots, fsrm.ifsrmrule_namespaceroots, fsrmpipeline/IFsrmRule::NamespaceRoots, fsrmpipeline/IFsrmRule::get_NamespaceRoots, fsrmpipeline/IFsrmRule::put_NamespaceRoots, get_NamespaceRoots
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: FsrmTemplateApplyOptions
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
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmRule::get_NamespaceRoots


## -description


An array of directory paths that the rule is applied to when classification is run.

This property is read/write.


## -parameters


## -remarks



All subdirectories under the specified path are also scanned (recursively).

Note that FSRM supports only NTFS file systems—you cannot specify paths on ReFS, FAT, 
    FAT32, UDF, or other non-NTFS file system.




## -see-also




<a href="https://msdn.microsoft.com/e1de871f-a2c9-4787-a3e8-8c3428e9249e">IFsrmRule</a>
 

 

