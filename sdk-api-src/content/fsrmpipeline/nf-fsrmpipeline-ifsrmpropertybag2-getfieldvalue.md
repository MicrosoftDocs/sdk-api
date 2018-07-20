---
UID: NF:fsrmpipeline.IFsrmPropertyBag2.GetFieldValue
title: IFsrmPropertyBag2::GetFieldValue
author: windows-sdk-content
description: Gets the value of the specified field from the property bag.
old-location: fsrm\ifsrmpropertybag2_getfieldvalue.htm
old-project: fsrm
ms.assetid: ccd52bbc-998e-435f-bea5-ed456adf3ff9
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: GetFieldValue, GetFieldValue method [File Server Resource Manager], GetFieldValue method [File Server Resource Manager],IFsrmPropertyBag2 interface, IFsrmPropertyBag2 interface [File Server Resource Manager],GetFieldValue method, IFsrmPropertyBag2.GetFieldValue, IFsrmPropertyBag2::GetFieldValue, fs.ifsrmpropertybag2_getfieldvalue, fsrm.ifsrmpropertybag2_getfieldvalue, fsrmpipeline/IFsrmPropertyBag2::GetFieldValue
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: fsrmpipeline.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: FsrmPipeline.idl
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
 - IFsrmPropertyBag2.GetFieldValue
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmPropertyBag2::GetFieldValue


## -description


Gets the value of the specified field from the property bag.


## -parameters




### -param field [in]

Type: <b><a href="https://msdn.microsoft.com/7a8cd6a6-7933-4190-b4fc-1b1cd653bd14">FsrmPropertyBagField</a></b>

Indicates whether the volume name returned is the name of the volume being accessed, which may be a snapshot, or the volume where the property bag lives.


### -param value [out, retval]

Type: <b>VARIANT*</b>

Returns the specified value.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/7a8cd6a6-7933-4190-b4fc-1b1cd653bd14">FsrmPropertyBagField</a>



<a href="https://msdn.microsoft.com/8f69556f-b96e-49b5-bc40-242768ebe767">IFsrmPropertyBag2</a>
 

 

