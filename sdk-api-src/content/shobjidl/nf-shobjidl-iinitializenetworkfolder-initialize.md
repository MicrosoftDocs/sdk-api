---
UID: NF:shobjidl.IInitializeNetworkFolder.Initialize
title: IInitializeNetworkFolder::Initialize
author: windows-sdk-content
description: Initializes a network folder, as specified.
old-location: shell\IInitializeNetworkFolder_Initialize.htm
old-project: shell
ms.assetid: a547b6f9-a4cc-4924-97f3-9fe08e6efc06
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IInitializeNetworkFolder interface [Windows Shell],Initialize method, IInitializeNetworkFolder.Initialize, IInitializeNetworkFolder::Initialize, Initialize, Initialize method [Windows Shell], Initialize method [Windows Shell],IInitializeNetworkFolder interface, _shell_IInitializeNetworkFolder_Initialize, shell.IInitializeNetworkFolder_Initialize, shobjidl/IInitializeNetworkFolder::Initialize
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: VPWATERMARKFLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl.h
api_name:
 - IInitializeNetworkFolder.Initialize
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# IInitializeNetworkFolder::Initialize


## -description


Initializes a network folder, as specified.


## -parameters




### -param pidl [in]

Type: <b>PCIDLIST_ABSOLUTE</b>

The Shell namespace location for this data source, as an IDList.


### -param pidlTarget [in]

Type: <b>PCIDLIST_ABSOLUTE</b>

The target namespace location, as an IDList. This is used when the data source is aliased into the namespace. This parameter specifies the location of the network item that the data source will represent. See <a href="https://msdn.microsoft.com/50a426b5-a526-4d3d-a20a-67050229f02e">InitializeEx</a> and in <a href="https://msdn.microsoft.com/74441551-c315-4203-a4f5-cd4e6c57b58b">PERSIST_FOLDER_TARGET_INFO</a> see the <i>pidlTargetFolder</i>   definition for more information.



### -param uDisplayType [in]

Type: <b>UINT</b>

The display type of the network resource this data source will represent. This is one of the RESOURCEDISPLAYTYPE_XXX values found in winnetwk.h.


### -param pszResName [in]

Type: <b>LPCWSTR</b>

The network resource name. for example, \\server or \\server\share. this is passed to the WNet in the <a href="https://msdn.microsoft.com/c53d078e-188a-4371-bdb9-fc023bc0c1ba">NETRESOURCE</a>.<i>lpRemoteName</i> field. 



### -param pszProvider [in, optional]

Type: <b>LPCWSTR</b>

Optional network provider, as in the <a href="https://msdn.microsoft.com/c53d078e-188a-4371-bdb9-fc023bc0c1ba">NETRESOURCE</a>.<i>lpProvider</i> field.



## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/65072af3-7583-4b15-b282-e7aa50cae3a8">IInitializeNetworkFolder</a>



<a href="https://msdn.microsoft.com/50a426b5-a526-4d3d-a20a-67050229f02e">InitializeEx</a>



<a href="https://msdn.microsoft.com/c53d078e-188a-4371-bdb9-fc023bc0c1ba">NETRESOURCE</a>



<a href="https://msdn.microsoft.com/74441551-c315-4203-a4f5-cd4e6c57b58b">PERSIST_FOLDER_TARGET_INFO</a>
 

 

