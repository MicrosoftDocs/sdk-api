---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IOfflineFilesConnectionInfo::SetConnectState


## -description



    Sets the connection state for an item.

Note that the entire scope of the item is transitioned, not just the item.  An item's  scope is defined as the closest ancestor shared folder of the item.


## -parameters




### -param hwndParent [in]

Provides a parent window handle used for any interactive user interface elements such as credential request dialogs.  This parameter may be <b>NULL</b>.  This parameter is ignored if the OFFLINEFILES_TRANSITION_FLAG_INTERACTIVE flag is not specified in the <i>dwFlags</i> parameter.


### -param dwFlags [in]

One or more of the following flag values:



#### OFFLINEFILES_TRANSITION_FLAG_INTERACTIVE (0x00000001)

Set this flag if the operation is allowed to display user interface elements as necessary.  An example is the system's credential-request dialog.  If this flag is set, the value in the <i>hwndParent</i> parameter is used as the parent window for any user interface elements displayed.



#### OFFLINEFILES_TRANSITION_FLAG_CONSOLE (0x00000002)

This flag is ignored if the OFFLINEFILES_TRANSITION_FLAG_INTERACTIVE flag is not set.  If the OFFLINEFILES_TRANSITION_FLAG_INTERACTIVE flag is set, this flag indicates that any UI produced should be directed to the console window associated with the process invoking the operation.


### -param ConnectState [in]

Specify one of the following <a href="https://msdn.microsoft.com/48c19b16-6ccb-4580-916d-0d23b69aafcf">OFFLINEFILES_CONNECT_STATE</a> enumeration values.



#### OFFLINEFILES_CONNECT_STATE_OFFLINE

Transition the item to offline.  Note that this operation will fail if there are currently open handles to affected files that are not cached by Offline Files.  The <a href="https://msdn.microsoft.com/cb32238d-c8f2-4228-8472-4a699b24c621">IOfflineFilesConnectionInfo::TransitionOffline</a> method allows you to control the closing of such handles.



#### OFFLINEFILES_CONNECT_STATE_ONLINE

Transitions the item online if possible.  This is equivalent to the <a href="https://msdn.microsoft.com/b8cac664-598d-43fd-a77e-e8406c197afc">IOfflineFilesConnectionInfo::TransitionOnline</a> method.


## -returns



Returns <b>S_OK</b> if successful, or an error value otherwise.




## -remarks



The <a href="https://msdn.microsoft.com/b8cac664-598d-43fd-a77e-e8406c197afc">IOfflineFilesConnectionInfo::TransitionOnline</a> and <a href="https://msdn.microsoft.com/cb32238d-c8f2-4228-8472-4a699b24c621">IOfflineFilesConnectionInfo::TransitionOffline</a> methods are preferred over this method as they provide greater control over the handling and detecting of open handles in the online-to-offline transition.




## -see-also




<a href="https://msdn.microsoft.com/923c5657-67e7-498a-a46b-97d44368cf3b">IOfflineFilesConnectionInfo</a>



<a href="https://msdn.microsoft.com/cb32238d-c8f2-4228-8472-4a699b24c621">IOfflineFilesConnectionInfo::TransitionOffline</a>



<a href="https://msdn.microsoft.com/b8cac664-598d-43fd-a77e-e8406c197afc">IOfflineFilesConnectionInfo::TransitionOnline</a>



<a href="https://msdn.microsoft.com/48c19b16-6ccb-4580-916d-0d23b69aafcf">OFFLINEFILES_CONNECT_STATE</a>
 

 

