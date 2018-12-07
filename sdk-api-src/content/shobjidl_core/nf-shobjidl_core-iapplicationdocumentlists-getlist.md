---
UID: NF:shobjidl_core.IApplicationDocumentLists.GetList
title: IApplicationDocumentLists::GetList
author: windows-sdk-content
description: Retrieves an object that represents the collection of destinations listed in the Recent or Frequent category in a Jump List.
old-location: shell\IApplicationDocumentLists_GetList.htm
tech.root: shell
ms.assetid: d86bf039-81d9-4d43-9671-b107d7e925ab
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ADLT_FREQUENT, ADLT_RECENT, GetList, GetList method [Windows Shell], GetList method [Windows Shell],IApplicationDocumentLists interface, IApplicationDocumentLists interface [Windows Shell],GetList method, IApplicationDocumentLists.GetList, IApplicationDocumentLists::GetList, _shell_IApplicationDocumentLists_GetList, shell.IApplicationDocumentLists_GetList, shobjidl_core/IApplicationDocumentLists::GetList
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
req.lib: Shell32.lib
req.dll: Shell32.dll (version 6.1 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IApplicationDocumentLists.GetList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IApplicationDocumentLists::GetList


## -description


Retrieves an object that represents the collection of destinations listed in the <b>Recent</b> or <b>Frequent</b> category in a Jump List.


## -parameters




### -param listtype [in]

Type: <b>APPDOCLISTTYPE</b>

One of the following values that specifies from which category the list of destinations should be retrieved.



#### ADLT_RECENT (0x0)

0x0. The <b>Recent</b> category, which lists those items most recently accessed.



#### ADLT_FREQUENT (0x1)

0x1. The <b>Frequent</b> category, which lists the items that have been accessed the greatest number of times.


### -param cItemsDesired [in]

Type: <b>UINT</b>

The number of items to retrieve from the list specified in <i>listtype</i>. Set this parameter to 0 to retrieve the full list.


### -param riid [in]

Type: <b>REFIID</b>

A reference to the IID of the interface to retrieve through <i>ppv</i>, typically IID_IObjectArray or IID_IEnumObjects.


### -param ppv [out]

Type: <b>void**</b>

When this method returns, contains the interface pointer requested in <i>riid</i>. This is typically an <a href="https://msdn.microsoft.com/ab0bb213-dc9c-4853-98d7-668e7ca76583">IObjectArray</a> or <a href="https://msdn.microsoft.com/914f2a4d-a67a-45d9-96ee-d8cae7d08e3c">IEnumObjects</a> which represents a collection of <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> or <a href="https://msdn.microsoft.com/67982d28-27ce-4482-b588-10fec8143750">IShellLink</a> objects (or a mix of the two) that represent the retrieved items from the list.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



An item can appear in both the <b>Recent</b> and <b>Frequent</b> lists.

If a user pins an item in the <b>Recent</b> or <b>Frequent</b> categories, the item is no longer shown in its original category to avoid duplication in the Jump List. However, the item will still be returned by this method.




## -see-also




<a href="https://msdn.microsoft.com/1912d8fd-1724-4a4b-b74a-e05db12ffead">IApplicationDocumentLists</a>



<a href="https://msdn.microsoft.com/1c5135c1-b98d-4d27-8437-5ca57af9a525">IApplicationDocumentLists::SetAppID</a>



<a href="https://msdn.microsoft.com/cbf2b07d-d67c-4755-888c-d40692d13cae">Taskbar Extensions</a>
 

 

