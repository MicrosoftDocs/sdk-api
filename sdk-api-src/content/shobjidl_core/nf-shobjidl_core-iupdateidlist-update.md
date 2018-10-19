---
UID: NF:shobjidl_core.IUpdateIDList.Update
title: IUpdateIDList::Update
author: windows-sdk-content
description: Updates the provided child ITEMIDLIST based on the parameters specified by the provided IBindCtx.
old-location: shell\IUpdateIDList_Update.htm
tech.root: shell
ms.assetid: 29f38464-bd16-4ee9-92b2-6697a3851f55
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: IUpdateIDList interface [Windows Shell],Update method, IUpdateIDList.Update, IUpdateIDList::Update, Update, Update method [Windows Shell], Update method [Windows Shell],IUpdateIDList interface, _shell_IUpdateIDList_Update, shell.IUpdateIDList_Update, shobjidl_core/IUpdateIDList::Update
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - shobjidl_core.h
api_name:
 - IUpdateIDList.Update
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUpdateIDList::Update


## -description


Updates the provided child <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> based on the parameters specified by the provided <a href="https://msdn.microsoft.com/e4c8abb5-0c89-44dd-8d95-efbfcc999b46">IBindCtx</a>.


## -parameters




### -param pbc [in, optional]

Type: <b><a href="https://msdn.microsoft.com/e4c8abb5-0c89-44dd-8d95-efbfcc999b46">IBindCtx</a>*</b>

An <a href="https://msdn.microsoft.com/e4c8abb5-0c89-44dd-8d95-efbfcc999b46">IBindCtx</a> interface on a bind context object. Used to specify parameters for updating the child <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a>. This value can be <b>NULL</b>.


### -param pidlIn [in]

Type: <b>PCUITEMID_CHILD</b>

The child <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a>.


### -param ppidlOut [out]

Type: <b>PITEMID_CHILD*</b>

A pointer to the child <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> relative to the parent folder.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If <i>pbc</i> is <b>NULL</b> or does not contain any parameters that apply to the current Shell folder, <i>ppidlOut</i> points to the same <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a>  as <i>pidlIn</i>.




## -see-also




<a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a>



<a href="https://msdn.microsoft.com/e6d94975-de33-497e-95a9-b89e8f8f0134">IUpdateIDList</a>
 

 

