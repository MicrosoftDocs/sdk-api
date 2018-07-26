---
UID: NF:shobjidl_core.ICustomDestinationList.BeginList
title: ICustomDestinationList::BeginList
author: windows-sdk-content
description: Initiates a building session for a custom Jump List.
old-location: shell\ICustomDestinationList_BeginList.htm
old-project: shell
ms.assetid: 431ae6b0-1421-46ec-a06a-38158acb0275
ms.author: windowssdkdev
ms.date: 07/20/2018
ms.keywords: BeginList, BeginList method [Windows Shell], BeginList method [Windows Shell],ICustomDestinationList interface, ICustomDestinationList interface [Windows Shell],BeginList method, ICustomDestinationList.BeginList, ICustomDestinationList::BeginList, _shell_ICustomDestinationList_BeginList, shell.ICustomDestinationList_BeginList, shobjidl_core/ICustomDestinationList::BeginList
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - ICustomDestinationList.BeginList
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 6.1 or later)
req.irql: 
req.product: Outlook Express 6.0
---

# ICustomDestinationList::BeginList


## -description


Initiates a building session for a custom Jump List.


## -parameters




### -param pcMinSlots [out]

Type: <b>UINT*</b>

A pointer that, when this method returns, points to the current user setting for the <b>Number of recent items to display in Jump Lists</b> option in the <b>Taskbar and Start Menu Properties</b> window. The default value is 10. This is the maximum number of destinations that will be shown, and it is a total of all destinations, regardless     of category. More destinations can be added, but they will not be shown in the UI.



A Jump List will always show at least this many slots—destinations and, if there is room, tasks.

This number does not include separators and section headers as long as the total number of separators and headers does not exceed four. Separators and section headers beyond the first four might reduce the number of destinations displayed if space is constrained. This number does not affect the standard command entries for pinning or unpinning, closing the window, or launching a new instance. It also does not affect tasks or pinned items, the number of which that can be displayed is based on the space available to the Jump List.


### -param riid [in]

Type: <b>REFIID</b>

A reference to the IID of an interface to be retrieved in <i>ppv</i>, typically IID_IObjectArray, that will represent all items currently stored in the list of removed destinations for the application. This information is used to ensure that removed items are not part of the new Jump List.


### -param ppv [out]

Type: <b>void**</b>

When this method returns, contains the interface pointer requested in <i>riid</i>. This is typically an <a href="https://msdn.microsoft.com/ab0bb213-dc9c-4853-98d7-668e7ca76583">IObjectArray</a>, which represents a collection of <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> and <a href="https://msdn.microsoft.com/67982d28-27ce-4482-b588-10fec8143750">IShellLink</a> objects that represent the removed items.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If an application has an explicit Application User Model ID (AppUserModelID), you must call <a href="https://msdn.microsoft.com/7b3a5d32-bf44-4c4f-9b31-6c0a82aac6fd">ICustomDestinationList::SetAppID</a> before you call this method.

The <a href="https://msdn.microsoft.com/ab0bb213-dc9c-4853-98d7-668e7ca76583">IObjectArray</a> interface retrieved in the <i>ppv</i> parameter represents the same list of removed destinations that is retrieved through <a href="https://msdn.microsoft.com/705763cf-a97f-430f-bfc3-916e943668ef">GetRemovedDestinations</a>. When a new Jump List is being generated, applications must first process any removed destinations. Tracking data for any item in the removed list must be cleared. If an application attempts to include an item through <a href="https://msdn.microsoft.com/091a2b28-b4cf-46a9-845a-46b5aa86522d">AppendCategory</a> that is present in this removed destinations list, the <b>AppendCategory</b> call fails. This ensures that applications respect the user's choice of removed items. After a call to <a href="https://msdn.microsoft.com/5f9aa598-9a94-4210-84cd-f4b39e47b260">CommitList</a> is made with no failed call to <b>AppendCategory</b> due to an attempt to re-add a removed item having been made since <b>BeginList</b>, the removed destinations list is cleared. After that time, a previously removed item can return to the destinations list if the user continues to use the item.

<b>BeginList</b> must be called to initiate the list before any calls are made to populate it through <a href="https://msdn.microsoft.com/091a2b28-b4cf-46a9-845a-46b5aa86522d">AppendCategory</a>, <a href="https://msdn.microsoft.com/ce73fff3-8d1a-4912-98ce-7149460ffa49">AppendKnownCategory</a>, or <a href="https://msdn.microsoft.com/7b254276-dc6f-4d20-8f44-fce8e01b237f">AddUserTasks</a>.




## -see-also




<a href="https://msdn.microsoft.com/65a3dab8-3136-416d-bd8a-ca813bfe0533">ICustomDestinationList</a>



<a href="https://msdn.microsoft.com/cbf2b07d-d67c-4755-888c-d40692d13cae">Taskbar Extensions</a>
 

 

