---
UID: NF:cscobj.IOfflineFilesConnectionInfo.TransitionOffline
title: IOfflineFilesConnectionInfo::TransitionOffline (cscobj.h)
description: Transitions an item offline if possible.
helpviewer_keywords: ["IOfflineFilesConnectionInfo interface [Offline Files]","TransitionOffline method","IOfflineFilesConnectionInfo.TransitionOffline","IOfflineFilesConnectionInfo::TransitionOffline","OFFLINEFILES_TRANSITION_FLAG_CONSOLE","OFFLINEFILES_TRANSITION_FLAG_INTERACTIVE","TransitionOffline","TransitionOffline method [Offline Files]","TransitionOffline method [Offline Files]","IOfflineFilesConnectionInfo interface","cscobj/IOfflineFilesConnectionInfo::TransitionOffline","of.iofflinefilesconnectioninfo_transitionoffline"]
old-location: of\iofflinefilesconnectioninfo_transitionoffline.htm
tech.root: of
ms.assetid: cb32238d-c8f2-4228-8472-4a699b24c621
ms.date: 12/05/2018
ms.keywords: IOfflineFilesConnectionInfo interface [Offline Files],TransitionOffline method, IOfflineFilesConnectionInfo.TransitionOffline, IOfflineFilesConnectionInfo::TransitionOffline, OFFLINEFILES_TRANSITION_FLAG_CONSOLE, OFFLINEFILES_TRANSITION_FLAG_INTERACTIVE, TransitionOffline, TransitionOffline method [Offline Files], TransitionOffline method [Offline Files],IOfflineFilesConnectionInfo interface, cscobj/IOfflineFilesConnectionInfo::TransitionOffline, of.iofflinefilesconnectioninfo_transitionoffline
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOfflineFilesConnectionInfo::TransitionOffline
 - cscobj/IOfflineFilesConnectionInfo::TransitionOffline
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CscSvc.dll
 - CscObj.dll
api_name:
 - IOfflineFilesConnectionInfo.TransitionOffline
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

<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesconnectioninfo">IOfflineFilesConnectionInfo</a>



<a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesconnectioninfo-transitiononline">IOfflineFilesConnectionInfo::TransitionOnline</a>