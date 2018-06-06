---
UID: NF:fsrmpipeline.IFsrmPropertyBag.GetFileProperty
title: IFsrmPropertyBag::GetFileProperty
author: windows-sdk-content
description: Retrieves the specified property from the property bag.
old-location: fsrm\ifsrmpropertybag_getfileproperty.htm
old-project: Fsrm
ms.assetid: 09fc3287-f2a2-4ba7-9626-65c6634b7f2d
ms.author: windowssdkdev
ms.date: 04/18/2018
ms.keywords: GetFileProperty, GetFileProperty method [File Server Resource Manager], GetFileProperty method [File Server Resource Manager],IFsrmPropertyBag interface, IFsrmPropertyBag interface [File Server Resource Manager],GetFileProperty method, IFsrmPropertyBag.GetFileProperty, IFsrmPropertyBag::GetFileProperty, fs.ifsrmpropertybag_getfileproperty, fsrm.ifsrmpropertybag_getfileproperty, fsrmpipeline/IFsrmPropertyBag::GetFileProperty
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
 - IFsrmPropertyBag.GetFileProperty
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmPropertyBag::GetFileProperty


## -description


Retrieves the specified property from the property bag.


## -parameters




### -param name [in]

The name of the property to retrieve.


### -param fileProperty [out]

An <a href="https://msdn.microsoft.com/feffccd1-cf72-45c0-97b3-d6efd736223e">IFsrmProperty</a> interface to the retrieved property.


## -returns



The method returns the following return values.




## -remarks



Use the property name specified in the rule's <a href="https://msdn.microsoft.com/0e41ac2b-c48a-4bb8-a363-8a64c856b8f9">PropertyAffected</a> property.




## -see-also




<a href="https://msdn.microsoft.com/237f024d-2b1d-45d5-a63d-c530426278e6">IFsrmPropertyBag</a>



<a href="https://msdn.microsoft.com/d3322907-c832-49ef-bf21-2e4581251a88">IFsrmPropertyBag::SetFileProperty</a>
 

 

