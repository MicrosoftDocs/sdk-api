---
UID: NF:cloneviewhelper.IViewHelper.Commit
title: IViewHelper::Commit
author: windows-sdk-content
description: The Commit method invalidates a Video Present Network (VidPN) on all graphics adapters.
old-location: display\iviewhelper_commit.htm
old-project: display
ms.assetid: f2d4ffcd-b1b4-419c-8c22-1f2561d77138
ms.author: windowssdkdev
ms.date: 06/26/2018
ms.keywords: Commit, Commit method [Display Devices], Commit method [Display Devices],IViewHelper interface, IViewHelper interface [Display Devices],Commit method, IViewHelper.Commit, IViewHelper::Commit, TMM_Ref_e3c1b7ef-16ad-4501-aba6-45e456bc7ac3.xml, cloneviewhelper/IViewHelper::Commit, display.iviewhelper_commit
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: cloneviewhelper.h
req.include-header: Cloneviewhelper.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: Windows 7
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: LOG_MANAGEMENT_CALLBACKS, *PLOG_MANAGEMENT_CALLBACKS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Cloneviewhelper.h
api_name:
 - IViewHelper.Commit
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IViewHelper::Commit


## -description


The <b>Commit</b> method invalidates a Video Present Network (VidPN) on all graphics adapters. 


## -parameters






## -returns



The <b>Commit</b> method returns one of the following values: 

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK </b></dt>
</dl>
</td>
<td width="60%">
<b>Commit</b> successfully invalidated a VidPN. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Any other error code (that is defined in <i>Winerror.h</i>) will cause TMM to not restore connections.</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
</table>
 




## -remarks



After <b>Commit</b> succeeds, the sources and targets on all of the graphics adapters are set. 

TMM calls <b>Commit</b> whenever a set of operations must be applied. For example, TMM might call <b>Commit</b> after a call to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff568174">IViewHelper::SetActiveTopology</a> method on a graphics adapter that requires for a source and targets to be mapped. TMM does not pass in the adapter name to <b>Commit</b> because the VidPN on all adapters should be invalidated. 

A call to <b>Commit</b> will no longer replace a call to <b>ChangeDisplaySettingsEx</b>(<b>NULL</b>, <b>NULL</b>, <b>NULL</b>, 0, <b>NULL</b>). However, TMM always ends its graphics operations with a <b>Commit</b> call. For more information about <b>ChangeDisplaySettingsEx</b>, see the Microsoft Windows SDK documentation. 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff568174">IViewHelper::SetActiveTopology</a>
 

 

