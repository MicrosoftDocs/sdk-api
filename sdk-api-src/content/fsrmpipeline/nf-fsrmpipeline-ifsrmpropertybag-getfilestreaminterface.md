---
UID: NF:fsrmpipeline.IFsrmPropertyBag.GetFileStreamInterface
title: IFsrmPropertyBag::GetFileStreamInterface (fsrmpipeline.h)
description: Retrieves a file stream interface that you can use to access the contents of the file.
helpviewer_keywords: ["GetFileStreamInterface","GetFileStreamInterface method [File Server Resource Manager]","GetFileStreamInterface method [File Server Resource Manager]","IFsrmPropertyBag interface","IFsrmPropertyBag interface [File Server Resource Manager]","GetFileStreamInterface method","IFsrmPropertyBag.GetFileStreamInterface","IFsrmPropertyBag::GetFileStreamInterface","fs.ifsrmpropertybag_getfilestreaminterface","fsrm.ifsrmpropertybag_getfilestreaminterface","fsrmpipeline/IFsrmPropertyBag::GetFileStreamInterface"]
old-location: fsrm\ifsrmpropertybag_getfilestreaminterface.htm
tech.root: fsrm
ms.assetid: e5250f0f-c8b4-4579-a4c2-b4f6ee48acdc
ms.date: 12/05/2018
ms.keywords: GetFileStreamInterface, GetFileStreamInterface method [File Server Resource Manager], GetFileStreamInterface method [File Server Resource Manager],IFsrmPropertyBag interface, IFsrmPropertyBag interface [File Server Resource Manager],GetFileStreamInterface method, IFsrmPropertyBag.GetFileStreamInterface, IFsrmPropertyBag::GetFileStreamInterface, fs.ifsrmpropertybag_getfilestreaminterface, fsrm.ifsrmpropertybag_getfilestreaminterface, fsrmpipeline/IFsrmPropertyBag::GetFileStreamInterface
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
 - IFsrmPropertyBag::GetFileStreamInterface
 - fsrmpipeline/IFsrmPropertyBag::GetFileStreamInterface
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
 - IFsrmPropertyBag.GetFileStreamInterface
---

# IFsrmPropertyBag::GetFileStreamInterface


## -description

Retrieves a file stream interface that you can use to access the contents of the file.

## -parameters

### -param accessMode [in]

One or more access modes. For possible values, see the 
      <a href="/windows/desktop/api/fsrmenums/ne-fsrmenums-fsrmfilestreamingmode">FsrmFileStreamingMode</a> enumeration.

### -param interfaceType [in]

The type of streaming interface to use. For possible interface types, see the 
      <a href="/windows/desktop/api/fsrmenums/ne-fsrmenums-fsrmfilestreaminginterfacetype">FsrmFileStreamingInterfaceType</a> 
      enumeration.

### -param pStreamInterface [out]

A <b>VARIANT</b> that contains the streaming interface that you can use to access the 
      contents of the file. The variant is of type <b>VT_DISPATCH</b>. Query the 
      <b>dispval</b> member of the variant to get the specified streaming interface.

## -returns

The method returns the following return values.

## -remarks

To ensure the caller can be authorized for access, it must be a module that has its 
    <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmpipelinemoduledefinition-get_needsfilecontent">IFsrmPipelineModuleDefinition::NeedsFileContent</a> 
    property set to <b>TRUE</b>. If the <i>accessMode</i> parameter is set to 
    <b>FsrmFileStreamingMode_Write</b>, the caller must also be a storage module and have its 
    <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmstoragemoduledefinition-get_updatesfilecontent">IFsrmStorageModuleDefinition::UpdatesFileContent</a> 
    property set to <b>TRUE</b>.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmpropertybag">IFsrmPropertyBag</a>