---
UID: NF:cscobj.IOfflineFilesConnectionInfo.TransitionOnline
title: IOfflineFilesConnectionInfo::TransitionOnline
author: windows-sdk-content
description: Transitions an item online if possible.
old-location: of\iofflinefilesconnectioninfo_transitiononline.htm
tech.root: OfflineFiles
ms.assetid: b8cac664-598d-43fd-a77e-e8406c197afc
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IOfflineFilesConnectionInfo interface [Offline Files],TransitionOnline method, IOfflineFilesConnectionInfo.TransitionOnline, IOfflineFilesConnectionInfo::TransitionOnline, OFFLINEFILES_TRANSITION_FLAG_CONSOLE, OFFLINEFILES_TRANSITION_FLAG_INTERACTIVE, TransitionOnline, TransitionOnline method [Offline Files], TransitionOnline method [Offline Files],IOfflineFilesConnectionInfo interface, cscobj/IOfflineFilesConnectionInfo::TransitionOnline, of.iofflinefilesconnectioninfo_transitiononline
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
 - IOfflineFilesConnectionInfo.TransitionOnline
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- cscobj.h
: 
- IOfflineFilesConnectionInfo.TransitionOnline
: 
---

# IOfflineFilesConnectionInfo::TransitionOnline


## -description


Transitions an item online if possible.


## -parameters




### -param hwndParent [in]

Provides a parent window handle used for any interactive user interface elements such as credential request dialogs.  This parameter may be <b>NULL</b>.  This parameter is ignored if the OFFLINEFILES_TRANSITION_FLAG_INTERACTIVE flag is not specified in the <i>dwFlags</i> parameter.


### -param dwFlags [in]

One or more of the following flag values:



#### OFFLINEFILES_TRANSITION_FLAG_INTERACTIVE (0x00000001)

Set this flag if the operation is allowed to display user interface elements as necessary.  An example is the system's credential-request dialog.  If this flag is set, the value in hwndParent is used as the parent for any user interface elements displayed.



#### OFFLINEFILES_TRANSITION_FLAG_CONSOLE (0x00000002)

This flag is ignored if the OFFLINEFILES_TRANSITION_FLAG_INTERACTIVE flag is not set.  If the OFFLINEFILES_TRANSITION_FLAG_INTERACTIVE flag is set, this flag indicates that any UI produced should be directed to the console window associated with the process invoking the operation.


## -returns



Returns <b>S_OK</b> if successful, or an error value otherwise.




## -remarks



Note that the entire scope of the item is transitioned online, not just the item.  An item's scope is defined as the closest ancestor shared folder of the item.




## -see-also




<a href="https://msdn.microsoft.com/923c5657-67e7-498a-a46b-97d44368cf3b">IOfflineFilesConnectionInfo</a>



<a href="https://msdn.microsoft.com/cb32238d-c8f2-4228-8472-4a699b24c621">IOfflineFilesConnectionInfo::TransitionOffline</a>
 

 

