---
UID: NF:fsrmpipeline.IFsrmPropertyBag.GetFileStreamInterface
title: IFsrmPropertyBag::GetFileStreamInterface
author: windows-driver-content
description: Retrieves a file stream interface that you can use to access the contents of the file.
old-location: fsrm\ifsrmpropertybag_getfilestreaminterface.htm
old-project: Fsrm
ms.assetid: e5250f0f-c8b4-4579-a4c2-b4f6ee48acdc
ms.author: windowsdriverdev
ms.date: 4/18/2018
ms.keywords: GetFileStreamInterface, GetFileStreamInterface method [File Server Resource Manager], GetFileStreamInterface method [File Server Resource Manager],IFsrmPropertyBag interface, IFsrmPropertyBag interface [File Server Resource Manager],GetFileStreamInterface method, IFsrmPropertyBag.GetFileStreamInterface, IFsrmPropertyBag::GetFileStreamInterface, fs.ifsrmpropertybag_getfilestreaminterface, fsrm.ifsrmpropertybag_getfilestreaminterface, fsrmpipeline/IFsrmPropertyBag::GetFileStreamInterface
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: FsrmTemplateApplyOptions
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	SrmSvc.dll
api_name:
-	IFsrmPropertyBag.GetFileStreamInterface
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmPropertyBag::GetFileStreamInterface


## -description


Retrieves a file stream interface that you can use to access the contents of the file.


## -parameters




### -param accessMode [in]

One or more access modes. For possible values, see the 
      <a href="https://msdn.microsoft.com/a2f7de78-7102-43f9-a7b8-b35ac0b7286a">FsrmFileStreamingMode</a> enumeration.


### -param interfaceType [in]

The type of streaming interface to use. For possible interface types, see the 
      <a href="https://msdn.microsoft.com/182dde15-f8d6-42ab-a9d2-85f0a0a4d670">FsrmFileStreamingInterfaceType</a> 
      enumeration.


### -param pStreamInterface






#### - streamInterface [out]

A <b>VARIANT</b> that contains the streaming interface that you can use to access the 
      contents of the file. The variant is of type <b>VT_DISPATCH</b>. Query the 
      <b>dispval</b> member of the variant to get the specified streaming interface.


## -returns



The method returns the following return values.




## -remarks



To ensure the caller can be authorized for access, it must be a module that has its 
    <a href="https://msdn.microsoft.com/c2cbcfe1-113c-4eb9-9dea-5619bcda58a2">IFsrmPipelineModuleDefinition::NeedsFileContent</a> 
    property set to <b>TRUE</b>. If the <i>accessMode</i> parameter is set to 
    <b>FsrmFileStreamingMode_Write</b>, the caller must also be a storage module and have its 
    <a href="https://msdn.microsoft.com/461befff-0bb4-44a2-9c37-e9a8fb1b080f">IFsrmStorageModuleDefinition::UpdatesFileContent</a> 
    property set to <b>TRUE</b>.




## -see-also




<a href="https://msdn.microsoft.com/237f024d-2b1d-45d5-a63d-c530426278e6">IFsrmPropertyBag</a>
 

 

