---
UID: NF:cloneviewhelper.IViewHelper.Commit
title: IViewHelper::Commit (cloneviewhelper.h)
description: The Commit method invalidates a Video Present Network (VidPN) on all graphics adapters.
helpviewer_keywords: ["Commit","Commit method [Display Devices]","Commit method [Display Devices]","IViewHelper interface","IViewHelper interface [Display Devices]","Commit method","IViewHelper.Commit","IViewHelper::Commit","TMM_Ref_e3c1b7ef-16ad-4501-aba6-45e456bc7ac3.xml","cloneviewhelper/IViewHelper::Commit","display.iviewhelper_commit"]
old-location: display\iviewhelper_commit.htm
tech.root: display
ms.assetid: f2d4ffcd-b1b4-419c-8c22-1f2561d77138
ms.date: 12/05/2018
ms.keywords: Commit, Commit method [Display Devices], Commit method [Display Devices],IViewHelper interface, IViewHelper interface [Display Devices],Commit method, IViewHelper.Commit, IViewHelper::Commit, TMM_Ref_e3c1b7ef-16ad-4501-aba6-45e456bc7ac3.xml, cloneviewhelper/IViewHelper::Commit, display.iviewhelper_commit
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IViewHelper::Commit
 - cloneviewhelper/IViewHelper::Commit
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Cloneviewhelper.h
api_name:
 - IViewHelper.Commit
---

# IViewHelper::Commit


## -description

The <b>Commit</b> method invalidates a Video Present Network (VidPN) on all graphics adapters.



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

TMM calls <b>Commit</b> whenever a set of operations must be applied. For example, TMM might call <b>Commit</b> after a call to the <a href="/previous-versions/windows/hardware/drivers/ff568174(v=vs.85)">IViewHelper::SetActiveTopology</a> method on a graphics adapter that requires for a source and targets to be mapped. TMM does not pass in the adapter name to <b>Commit</b> because the VidPN on all adapters should be invalidated. 

A call to <b>Commit</b> will no longer replace a call to <b>ChangeDisplaySettingsEx</b>(<b>NULL</b>, <b>NULL</b>, <b>NULL</b>, 0, <b>NULL</b>). However, TMM always ends its graphics operations with a <b>Commit</b> call. For more information about <b>ChangeDisplaySettingsEx</b>, see the Microsoft Windows SDK documentation.

## -see-also

<a href="/previous-versions/windows/hardware/drivers/ff568174(v=vs.85)">IViewHelper::SetActiveTopology</a>
