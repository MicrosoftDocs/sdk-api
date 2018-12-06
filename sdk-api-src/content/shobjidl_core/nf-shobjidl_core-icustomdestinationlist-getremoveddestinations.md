---
UID: NF:shobjidl_core.ICustomDestinationList.GetRemovedDestinations
title: ICustomDestinationList::GetRemovedDestinations
author: windows-sdk-content
description: Retrieves the current list of destinations that have been removed by the user from the existing Jump List that this custom Jump List is meant to replace.
old-location: shell\ICustomDestinationList_GetRemovedDestinations.htm
tech.root: shell
ms.assetid: 705763cf-a97f-430f-bfc3-916e943668ef
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetRemovedDestinations, GetRemovedDestinations method [Windows Shell], GetRemovedDestinations method [Windows Shell],ICustomDestinationList interface, ICustomDestinationList interface [Windows Shell],GetRemovedDestinations method, ICustomDestinationList.GetRemovedDestinations, ICustomDestinationList::GetRemovedDestinations, _shell_ICustomDestinationList_GetRemovedDestinations, shell.ICustomDestinationList_GetRemovedDestinations, shobjidl_core/ICustomDestinationList::GetRemovedDestinations
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
 - ICustomDestinationList.GetRemovedDestinations
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICustomDestinationList::GetRemovedDestinations


## -description


Retrieves the current list of destinations that have been removed by the user from the existing Jump List that this custom Jump List is meant to replace.


## -parameters




### -param riid [in]

Type: <b>REFIID</b>

A reference to the IID of the interface to retrieve through <i>ppv</i>, typically IID_IObjectArray.


### -param ppv [out]

Type: <b>void**</b>

When this method returns, contains the interface pointer requested in <i>riid</i>. This is typically an <a href="https://msdn.microsoft.com/ab0bb213-dc9c-4853-98d7-668e7ca76583">IObjectArray</a>, which represents a collection of <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> or <a href="https://msdn.microsoft.com/67982d28-27ce-4482-b588-10fec8143750">IShellLink</a> objects that represent the items in the list of removed destinations.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Items can be removed from the Jump List UI through user action. The item is then marked as removed and is no longer displayed. An application can use this method to tell which items the user has removed so that it knows not to show them in its custom list. For instance, this method should be called when an application is launched, if that application is not going to generate a new list through <a href="https://msdn.microsoft.com/431ae6b0-1421-46ec-a06a-38158acb0275">ICustomDestinationList::BeginList</a>.

It is strongly recommended that an application clear any destination tracking data when the user elects to remove that destination. If the user accesses that destination again in the future, it may be re-added to the Jump List and can again accumulate data. The same removed destinations list retrieved by this method is retrieved when <a href="https://msdn.microsoft.com/431ae6b0-1421-46ec-a06a-38158acb0275">ICustomDestinationList::BeginList</a> is called. In that case, the application must not immediately attempt to reinsert any removed item or that call to <a href="https://msdn.microsoft.com/091a2b28-b4cf-46a9-845a-46b5aa86522d">AppendCategory</a> will fail. This ensures that the application respects the user's intent to remove the item.

If the application has an explicit Application User Model ID (AppUserModelID), you must call <a href="https://msdn.microsoft.com/7b3a5d32-bf44-4c4f-9b31-6c0a82aac6fd">SetAppID</a> before calling this method.

Even if an application calls <b>GetRemovedDestinations</b> and finds an item on the list that has a high probability to be restored to the Jump List sooner than a new custom Jump List is expected to be created, the application should write the Jump List without that item and re-add it to the list only after the user has again accessed it.

An application can add a <b>Recent</b> or <b>Frequent</b> <a href="https://msdn.microsoft.com/ce73fff3-8d1a-4912-98ce-7149460ffa49">known category</a> to its custom Jump List. Items in that category might be in the removed items list even though they were not shown in any custom category. In that case, the application should still clear any usage data for that item if any had been stored.

A call to <b>GetRemovedDestinations</b> does not clear the removed destinations data. This data is needed by <a href="https://msdn.microsoft.com/431ae6b0-1421-46ec-a06a-38158acb0275">BeginList</a> for its next list generation. The removed destinations data is no longer needed and is cleared after a list generation session is begun by <b>BeginList</b>, continued with no failed calls to <b>AppendCategory</b>, and completed by a call to <a href="https://msdn.microsoft.com/5f9aa598-9a94-4210-84cd-f4b39e47b260">CommitList</a>.




## -see-also




<a href="https://msdn.microsoft.com/65a3dab8-3136-416d-bd8a-ca813bfe0533">ICustomDestinationList</a>



<a href="https://msdn.microsoft.com/431ae6b0-1421-46ec-a06a-38158acb0275">ICustomDestinationList::BeginList</a>



<a href="https://msdn.microsoft.com/cbf2b07d-d67c-4755-888c-d40692d13cae">Taskbar Extensions</a>
 

 

