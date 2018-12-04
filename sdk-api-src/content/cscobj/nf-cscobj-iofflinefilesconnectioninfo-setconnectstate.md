---
UID: NF:cscobj.IOfflineFilesConnectionInfo.SetConnectState
title: IOfflineFilesConnectionInfo::SetConnectState
author: windows-sdk-content
description: Sets the connection state for an item.
old-location: of\iofflinefilesconnectioninfo_setconnectstate.htm
tech.root: offlinefiles
ms.assetid: 42412f42-7a70-4110-88ec-a38b3df7d2da
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IOfflineFilesConnectionInfo interface [Offline Files],SetConnectState method, IOfflineFilesConnectionInfo.SetConnectState, IOfflineFilesConnectionInfo::SetConnectState, OFFLINEFILES_CONNECT_STATE_OFFLINE, OFFLINEFILES_CONNECT_STATE_ONLINE, OFFLINEFILES_TRANSITION_FLAG_CONSOLE, OFFLINEFILES_TRANSITION_FLAG_INTERACTIVE, SetConnectState, SetConnectState method [Offline Files], SetConnectState method [Offline Files],IOfflineFilesConnectionInfo interface, cscobj/IOfflineFilesConnectionInfo::SetConnectState, of.iofflinefilesconnectioninfo_setconnectstate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: cscobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
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
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CscSvc.dll
 - CscObj.dll
api_name:
 - IOfflineFilesConnectionInfo.SetConnectState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

