---
UID: NF:fsrm.IFsrmPathMapper.GetSharePathsForLocalPath
title: IFsrmPathMapper::GetSharePathsForLocalPath (fsrm.h)
description: Retrieves a list of network shares that point to the specified local path.
helpviewer_keywords: ["FsrmPathMapper class [File Server Resource Manager]","GetSharePathsForLocalPath method","GetSharePathsForLocalPath","GetSharePathsForLocalPath method [File Server Resource Manager]","GetSharePathsForLocalPath method [File Server Resource Manager]","FsrmPathMapper class","GetSharePathsForLocalPath method [File Server Resource Manager]","IFsrmPathMapper interface","IFsrmPathMapper interface [File Server Resource Manager]","GetSharePathsForLocalPath method","IFsrmPathMapper.GetSharePathsForLocalPath","IFsrmPathMapper::GetSharePathsForLocalPath","fs.ifsrmpathmapper_getsharepathsforlocalpath","fsrm.ifsrmpathmapper_getsharepathsforlocalpath","fsrm/IFsrmPathMapper::GetSharePathsForLocalPath"]
old-location: fsrm\ifsrmpathmapper_getsharepathsforlocalpath.htm
tech.root: fsrm
ms.assetid: af5c668f-4675-4568-9b6a-c8d2663d819b
ms.date: 12/05/2018
ms.keywords: FsrmPathMapper class [File Server Resource Manager],GetSharePathsForLocalPath method, GetSharePathsForLocalPath, GetSharePathsForLocalPath method [File Server Resource Manager], GetSharePathsForLocalPath method [File Server Resource Manager],FsrmPathMapper class, GetSharePathsForLocalPath method [File Server Resource Manager],IFsrmPathMapper interface, IFsrmPathMapper interface [File Server Resource Manager],GetSharePathsForLocalPath method, IFsrmPathMapper.GetSharePathsForLocalPath, IFsrmPathMapper::GetSharePathsForLocalPath, fs.ifsrmpathmapper_getsharepathsforlocalpath, fsrm.ifsrmpathmapper_getsharepathsforlocalpath, fsrm/IFsrmPathMapper::GetSharePathsForLocalPath
req.header: fsrm.h
req.include-header: FsrmPipeline.h, FsrmQuota.h, FsrmReports.h, FsrmScreen.h, FsrmTlb.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
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
 - IFsrmPathMapper::GetSharePathsForLocalPath
 - fsrm/IFsrmPathMapper::GetSharePathsForLocalPath
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
 - IFsrmPathMapper.GetSharePathsForLocalPath
 - FsrmPathMapper.GetSharePathsForLocalPath
---

# IFsrmPathMapper::GetSharePathsForLocalPath


## -description

Retrieves a list of network shares that point to the specified local path.

## -parameters

### -param localPath [in]

The local path. The string is limited to 260 characters.

### -param sharePaths [out]

A <b>SAFEARRAY</b> of <b>VARIANT</b>s. Each 
      <b>VARIANT</b> contains a network share path that points to the local path. The variant 
      type is <b>VT_BSTR</b>. Use the <b>bstrVal</b> member to access the share 
      path.

## -returns

The method returns the following return values.

## -remarks

When you get the path property for a quota, the path is the local path. You use this method to convert that 
    local path to the network path if you want to know the actual network share that is running out of space.

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrmpathmapper">FsrmPathMapper</a>



<a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmpathmapper">IFsrmPathMapper</a>