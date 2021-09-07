---
UID: NF:shobjidl.IInitializeNetworkFolder.Initialize
title: IInitializeNetworkFolder::Initialize (shobjidl.h)
description: Initializes a network folder, as specified.
helpviewer_keywords: ["IInitializeNetworkFolder interface [Windows Shell]","Initialize method","IInitializeNetworkFolder.Initialize","IInitializeNetworkFolder::Initialize","Initialize","Initialize method [Windows Shell]","Initialize method [Windows Shell]","IInitializeNetworkFolder interface","_shell_IInitializeNetworkFolder_Initialize","shell.IInitializeNetworkFolder_Initialize","shobjidl/IInitializeNetworkFolder::Initialize"]
old-location: shell\IInitializeNetworkFolder_Initialize.htm
tech.root: shell
ms.assetid: a547b6f9-a4cc-4924-97f3-9fe08e6efc06
ms.date: 12/05/2018
ms.keywords: IInitializeNetworkFolder interface [Windows Shell],Initialize method, IInitializeNetworkFolder.Initialize, IInitializeNetworkFolder::Initialize, Initialize, Initialize method [Windows Shell], Initialize method [Windows Shell],IInitializeNetworkFolder interface, _shell_IInitializeNetworkFolder_Initialize, shell.IInitializeNetworkFolder_Initialize, shobjidl/IInitializeNetworkFolder::Initialize
f1_keywords:
- shobjidl/IInitializeNetworkFolder.Initialize
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Shobjidl.h
api_name:
- IInitializeNetworkFolder.Initialize
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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

The target namespace location, as an IDList. This is used when the data source is aliased into the namespace. This parameter specifies the location of the network item that the data source will represent. See <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder3-initializeex">InitializeEx</a> and in <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-persist_folder_target_info">PERSIST_FOLDER_TARGET_INFO</a> see the <i>pidlTargetFolder</i>   definition for more information.



### -param uDisplayType [in]

Type: <b>UINT</b>

The display type of the network resource this data source will represent. This is one of the RESOURCEDISPLAYTYPE_XXX values found in winnetwk.h.


### -param pszResName [in]

Type: <b>LPCWSTR</b>

The network resource name. for example, \\server or \\server\share. this is passed to the WNet in the <a href="/windows/desktop/api/rrascfg/nn-rrascfg-ieapproviderconfig">NETRESOURCE</a>.<i>lpRemoteName</i> field. 



### -param pszProvider [in, optional]

Type: <b>LPCWSTR</b>

Optional network provider, as in the <a href="/windows/desktop/api/rrascfg/nn-rrascfg-ieapproviderconfig">NETRESOURCE</a>.<i>lpProvider</i> field.



## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="/windows/desktop/api/shobjidl/nn-shobjidl-iinitializenetworkfolder">IInitializeNetworkFolder</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder3-initializeex">InitializeEx</a>



<a href="/windows/desktop/api/rrascfg/nn-rrascfg-ieapproviderconfig">NETRESOURCE</a>



<a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-persist_folder_target_info">PERSIST_FOLDER_TARGET_INFO</a>
 

 