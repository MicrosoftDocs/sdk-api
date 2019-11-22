---
UID: NN:mobsync.ISyncMgrSynchronize
title: ISyncMgrSynchronize (mobsync.h)

description: Exposes methods that enable the registered application or service to receive notifications from the synchronization manager.
old-location: shell\syncmgr_isyncmgrsynchronize.htm
tech.root: shell
ms.assetid: bb821672-10b1-4fe6-a752-6cd1ccd1e49e

ms.date: 12/05/2018
ms.keywords: ISyncMgrSynchronize, ISyncMgrSynchronize interface [Windows Shell], ISyncMgrSynchronize interface [Windows Shell],described, mobsync/ISyncMgrSynchronize, shell.syncmgr_isyncmgrsynchronize, syncmgr.isyncmgrsynchronize
ms.topic: interface
f1_keywords: 
 - "mobsync/ISyncMgrSynchronize"
dev_langs:
 - c++
req.header: mobsync.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: Mobsync.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mobsync.dll
api_name:
 - ISyncMgrSynchronize
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISyncMgrSynchronize interface


## -description


Exposes methods that enable the registered application or service to receive notifications from the synchronization manager.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncMgrSynchronize</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISyncMgrSynchronize</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISyncMgrSynchronize</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-enumsyncmgritems">EnumSyncMgrItems</a>
</td>
<td align="left" width="63%">
Obtains the 
<a href="https://docs.microsoft.com/windows/desktop/api/mobsync/nn-mobsync-isyncmgrenumitems">ISyncMgrEnumItems</a> interface for the items that are handled by a registered application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-gethandlerinfo">GetHandlerInfo</a>
</td>
<td align="left" width="63%">
Obtains handler information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-getitemobject">GetItemObject</a>
</td>
<td align="left" width="63%">
Obtains an interface on a specified item that a registered application handles.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Called by the synchronization manager in a registered application handler to determine whether the handler processes the synchronization event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-prepareforsync">PrepareForSync</a>
</td>
<td align="left" width="63%">
Allows a registered application to display any user interface, and perform any necessary initialization before the <a href="https://docs.microsoft.com/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-synchronize">ISyncMgrSynchronize::Synchronize</a> method is called. For example, an application such as the Outlook email client may need to display the password dialog box to enable a user to log on to a mail server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-setitemstatus">SetItemStatus</a>
</td>
<td align="left" width="63%">
Called by the synchronization manager in a registered application's handler to change the status of an item in the following two cases: between the time the handler has returned from the <a href="https://docs.microsoft.com/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-prepareforsync">ISyncMgrSynchronize::PrepareForSync</a> method and called the 
<a href="https://docs.microsoft.com/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronizecallback-prepareforsynccompleted">ISyncMgrSynchronizeCallback::PrepareForSyncCompleted</a> callback method, or after the handler has returned from the <a href="https://docs.microsoft.com/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-synchronize">ISyncMgrSynchronize::Synchronize</a> method but has not yet called the <a href="https://docs.microsoft.com/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronizecallback-synchronizecompleted">ISyncMgrSynchronizeCallback::SynchronizeCompleted</a> callback method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-setprogresscallback">SetProgressCallback</a>
</td>
<td align="left" width="63%">
Sets the <a href="https://docs.microsoft.com/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronizecallback">ISyncMgrSynchronizeCallback</a> interface. Registered applications use this callback interface to give status information from within the <a href="https://docs.microsoft.com/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-prepareforsync">ISyncMgrSynchronize::PrepareForSync</a> and <a href="https://docs.microsoft.com/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-synchronize">ISyncMgrSynchronize::Synchronize</a> methods.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-showerror">ShowError</a>
</td>
<td align="left" width="63%">
Called by the synchronization manager in a registered application handler when a user double-clicks an associated message in the error tab.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-showproperties">ShowProperties</a>
</td>
<td align="left" width="63%">
Called by the synchronization manager when a user selects an item in the choice dialog box, and then clicks the <b>Properties</b> button.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-synchronize">Synchronize</a>
</td>
<td align="left" width="63%">
Called by the synchronization manager once for each selected group after the user has chosen the registered applications to be synchronized.

</td>
</tr>
</table> 


## -remarks



<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
This interface should be implemented on the registered application's handler to receive notifications from the synchronization manager and to participate in the synchronization process.

<b>ISyncMgrSynchronize</b> has been replaced in Windows Vista by <a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrhandler">ISyncMgrHandler</a>.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
The synchronization manager calls the methods of this interface to send notifications to the registered application or service during synchronization.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mobsync/nn-mobsync-isyncmgrenumitems">ISyncMgrEnumItems</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronizecallback">ISyncMgrSynchronizeCallback</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronizeinvoke">ISyncMgrSynchronizeInvoke</a>
 

 

