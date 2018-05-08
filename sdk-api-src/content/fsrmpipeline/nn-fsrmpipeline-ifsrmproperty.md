---
UID: NN:fsrmpipeline.IFsrmProperty
title: IFsrmProperty
author: windows-driver-content
description: Defines an instance of a property.
old-location: fsrm\ifsrmproperty.htm
old-project: Fsrm
ms.assetid: feffccd1-cf72-45c0-97b3-d6efd736223e
ms.author: windowsdriverdev
ms.date: 4/18/2018
ms.keywords: IFsrmProperty, IFsrmProperty interface [File Server Resource Manager], IFsrmProperty interface [File Server Resource Manager],described, fs.ifsrmproperty, fsrm.ifsrmproperty, fsrm/IFsrmProperty
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: fsrmpipeline.h
req.include-header: FsrmPipeline.h, FsrmQuota.h, FsrmReports.h, FsrmScreen.h
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
req.typenames: FsrmTemplateApplyOptions
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	SrmSvc.dll
api_name:
-	IFsrmProperty
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmProperty interface


## -description


Defines an instance of a property.

The following methods return this interface:
<ul>
<li>
<a href="https://msdn.microsoft.com/c8a3c4cb-4753-495b-88f4-2d6cdfef7dc7">IFsrmClassificationManager::GetFileProperty</a>
</li>
<li>
<a href="https://msdn.microsoft.com/09fc3287-f2a2-4ba7-9626-65c6634b7f2d">IFsrmPropertyBag::GetFileProperty</a>
</li>
<li>
<a href="https://msdn.microsoft.com/9a833e94-d26b-4c94-bf2f-76ac6db3f8e9">IFsrmClassificationManager::EnumFileProperties</a>
</li>
</ul>
