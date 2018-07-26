---
UID: NF:fsrm.IFsrmPathMapper.GetSharePathsForLocalPath
title: IFsrmPathMapper::GetSharePathsForLocalPath
author: windows-sdk-content
description: Retrieves a list of network shares that point to the specified local path.
old-location: fsrm\ifsrmpathmapper_getsharepathsforlocalpath.htm
old-project: Fsrm
ms.assetid: af5c668f-4675-4568-9b6a-c8d2663d819b
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: FsrmPathMapper class [File Server Resource Manager],GetSharePathsForLocalPath method, GetSharePathsForLocalPath, GetSharePathsForLocalPath method [File Server Resource Manager], GetSharePathsForLocalPath method [File Server Resource Manager],FsrmPathMapper class, GetSharePathsForLocalPath method [File Server Resource Manager],IFsrmPathMapper interface, IFsrmPathMapper interface [File Server Resource Manager],GetSharePathsForLocalPath method, IFsrmPathMapper.GetSharePathsForLocalPath, IFsrmPathMapper::GetSharePathsForLocalPath, fs.ifsrmpathmapper_getsharepathsforlocalpath, fsrm.ifsrmpathmapper_getsharepathsforlocalpath, fsrm/IFsrmPathMapper::GetSharePathsForLocalPath
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: FILTERED_DATA_SOURCES
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
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
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




<a href="https://msdn.microsoft.com/19f7f1d1-7d10-4b73-a158-7c8722958ab5">FsrmPathMapper</a>



<a href="https://msdn.microsoft.com/04e62a10-1719-454b-adfb-6320e31c7a88">IFsrmPathMapper</a>
 

 

