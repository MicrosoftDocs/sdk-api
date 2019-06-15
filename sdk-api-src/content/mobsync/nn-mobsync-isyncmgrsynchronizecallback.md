---
UID: NN:mobsync.ISyncMgrSynchronizeCallback
title: ISyncMgrSynchronizeCallback (mobsync.h)
author: windows-sdk-content
description: Exposes methods that manage the synchronization process.
old-location: shell\syncmgr_isyncmgrsynchronizecallback.htm
tech.root: shell
ms.assetid: 1c817a21-be91-43af-86c8-aa7909ae2fa2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISyncMgrSynchronizeCallback, ISyncMgrSynchronizeCallback interface [Windows Shell], ISyncMgrSynchronizeCallback interface [Windows Shell],described, mobsync/ISyncMgrSynchronizeCallback, shell.syncmgr_isyncmgrsynchronizecallback, syncmgr.isyncmgrsynchronizecallback
ms.topic: interface
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
 - ISyncMgrSynchronizeCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISyncMgrSynchronizeCallback interface


## -description


Exposes methods that manage the synchronization process.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncMgrSynchronizeCallback</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISyncMgrSynchronizeCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISyncMgrSynchronizeCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronizecallback-deletelogerror">DeleteLogError</a>
</td>
<td align="left" width="63%">
Called by the registered application's handler to delete a previously logged ErrorInformation, warning, or error message in the error tab on the synchronization manager status dialog box.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronizecallback-enablemodeless">EnableModeless</a>
</td>
<td align="left" width="63%">
Called by the registered application before and after any dialog boxes are displayed from within the <a href="https://docs.microsoft.com/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-prepareforsync">ISyncMgrSynchronize::PrepareForSync</a> and 
<a href="https://docs.microsoft.com/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-synchronize">ISyncMgrSynchronize::Synchronize</a> methods.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronizecallback-establishconnection">EstablishConnection</a>
</td>
<td align="left" width="63%">
Called by the registered application's handler when a network connection is required.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronizecallback-logerror">LogError</a>
</td>
<td align="left" width="63%">
Called by a registered application to log information, warning, or an error message into the error tab on the synchronization manager status dialog box.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronizecallback-prepareforsynccompleted">PrepareForSyncCompleted</a>
</td>
<td align="left" width="63%">
Called by a registered handler of an application after the 
<a href="https://docs.microsoft.com/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-prepareforsync">ISyncMgrSynchronize::PrepareForSync</a> method is complete.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronizecallback-progress">Progress</a>
</td>
<td align="left" width="63%">
Called by a registered application to update the progress information and determine whether an operation should continue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronizecallback-showerrorcompleted">ShowErrorCompleted</a>
</td>
<td align="left" width="63%">
Called by the registered application's handler before or after its <a href="https://docs.microsoft.com/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-prepareforsync">ISyncMgrSynchronize::PrepareForSync</a> operation has been completed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronizecallback-showpropertiescompleted">ShowPropertiesCompleted</a>
</td>
<td align="left" width="63%">
Called by the registered application's handler before or after its 
<a href="https://docs.microsoft.com/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-showproperties">ISyncMgrSynchronize::ShowProperties</a> operation is completed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronizecallback-synchronizecompleted">SynchronizeCompleted</a>
</td>
<td align="left" width="63%">
Called by an application when its <a href="https://docs.microsoft.com/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-synchronize">ISyncMgrSynchronize::Synchronize</a> method is complete.

</td>
</tr>
</table> 


## -remarks



<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
This interface is implemented by the synchronization manager to receive status, error, and progress information and display the user interface during the synchronization process.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
Applications should call the methods of this interface as often as possible and must call it before starting each new ItemID to check whether the user has canceled an individual item.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronize">ISyncMgrSynchronize</a>
 

 

