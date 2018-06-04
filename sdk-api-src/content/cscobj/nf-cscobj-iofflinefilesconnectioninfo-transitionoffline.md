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

# IOfflineFilesConnectionInfo::TransitionOffline


## -description


Transitions an item offline if possible.


## -parameters




### -param hwndParent [in]

Provides a parent window handle used for any interactive user interface elements such as credential request dialogs.  This parameter may be <b>NULL</b>.  This parameter is ignored if the <b>OFFLINEFILES_TRANSITION_FLAG_INTERACTIVE</b> flag is not set.


### -param dwFlags [in]

One or more of the following flag values:



#### OFFLINEFILES_TRANSITION_FLAG_INTERACTIVE (0x00000001)

Set this flag if the operation is allowed to display user interface elements as necessary.  An example is the system's credential-request dialog.  If this flag is set, the value in <i>hwndParent</i> is used as the parent for any user interface elements displayed.



#### OFFLINEFILES_TRANSITION_FLAG_CONSOLE (0x00000002)

This flag is ignored if the <b>OFFLINEFILES_TRANSITION_FLAG_INTERACTIVE</b> flag is not set.  If the <b>OFFLINEFILES_TRANSITION_FLAG_INTERACTIVE</b> flag is set, this flag indicates that any UI produced should be directed to the console window associated with the process invoking the operation.


### -param bForceOpenFilesClosed [in]

By default, any open handles to files that are not cached by Offline Files prevent the transition to offline.  If this parameter is <b>TRUE</b>, the operation will forcibly close these files handles, allowing the scope to transition offline.

<div class="alert"><b>Note</b>  If file handles are forcibly closed, this can cause unexpected consequences, depending on the applications that are using those files.</div>
<div> </div>

### -param pbOpenFilesPreventedTransition [out]

Receives <b>TRUE</b> if open files prevented the transition, or <b>FALSE</b> otherwise.  This value is useful only if <b>FALSE</b> was specified for the <i>bForceOpenFilesClosed</i> parameter.


## -returns



Returns <b>S_OK</b> if successful, or an error value otherwise.




## -remarks



Note that the entire scope of the item is transitioned offline, not just the item.  An item's scope is defined as the closest ancestor shared folder of the item.

If open handles prevent the offline transition, the function returns a success value and <i>*pbOpenFilesPreventTransition</i> receives <b>TRUE</b>.

Here is an example of how this method is used: When transitioning a scope offline through Windows Vista Explorer's Work Offline button, this method is first called with the <i>bForceOpenFilesClosed</i> parameter set to <b>FALSE</b>.  If the function indicates that open files prevented the offline transition, Windows Explorer presents a dialog asking the user if they want to force those files closed and repeat the attempt.  If they respond affirmatively, the function call is repeated with the <i>bForceOpenFilesClosed</i> parameter set to <b>TRUE</b>.




## -see-also




<a href="https://msdn.microsoft.com/923c5657-67e7-498a-a46b-97d44368cf3b">IOfflineFilesConnectionInfo</a>



<a href="https://msdn.microsoft.com/b8cac664-598d-43fd-a77e-e8406c197afc">IOfflineFilesConnectionInfo::TransitionOnline</a>
 

 

