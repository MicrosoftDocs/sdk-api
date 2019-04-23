---
UID: NN:mmc.IConsole
title: IConsole (mmc.h)
author: windows-sdk-content
description: Enables communication with the console.
old-location: mmc\iconsole.htm
tech.root: mmc
ms.assetid: 65154EB1-ABE5-4C4F-8B09-08633D82FD62
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IConsole, IConsole interface [MMC], IConsole interface [MMC],described, mmc.iconsole, mmc/IConsole
ms.topic: interface
req.header: mmc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mmc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Mmcndmgr.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmcndmgr.dll
api_name:
 - IConsole
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IConsole interface


## -description


<div class="alert"><b>Note</b>  This interface is obsolete, and only used in MMC 1.0.</div><div> </div>Enables communication with the console.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IConsole</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IConsole</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IConsole</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/en-us/windows/desktop/api/mmc/nf-mmc-iconsole-getmainwindow">GetMainWindow</a>
</td>
<td align="left" width="63%">
Returns a handle to the main frame window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms645505(v=VS.85).aspx">MessageBox</a>
</td>
<td align="left" width="63%">
Displays a message box.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/en-us/windows/desktop/api/mmc/nf-mmc-iconsole-newwindow">NewWindow</a>
</td>
<td align="left" width="63%">
Creates a new window rooted at the specified scope item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/en-us/windows/desktop/api/mmc/nf-mmc-iconsole-queryconsoleverb">QueryConsoleVerb</a>
</td>
<td align="left" width="63%">
Query for the 
<a href="https://msdn.microsoft.com/9c4338c1-eb5e-47f3-8b5b-0623690bd5f6">IConsoleVerb</a> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/en-us/windows/desktop/api/mmc/nf-mmc-iconsole-queryresultimagelist">QueryResultImageList</a>
</td>
<td align="left" width="63%">
Queries the console-provided result pane's image list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/en-us/windows/desktop/api/mmc/nf-mmc-iconsole-queryresultview">QueryResultView</a>
</td>
<td align="left" width="63%">
Queries IConsole for the result view object's <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface pointer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6c21d454-2d3f-4e10-a4b0-135d20aea669">QueryScopeImageList</a>
</td>
<td align="left" width="63%">
Queries the console-provided scope pane's image list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/en-us/windows/desktop/api/mmc/nf-mmc-iconsole-selectscopeitem">SelectScopeItem</a>
</td>
<td align="left" width="63%">
Selects the given scope item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/en-us/windows/desktop/api/mmc/nf-mmc-iconsole-setheader">SetHeader</a>
</td>
<td align="left" width="63%">
Used by instances of 
<a href="https://msdn.microsoft.com/65eaa5ef-182b-4fec-bb3d-a308ac9dc660">IComponent</a> only. Sets the header interface to be used for this 
IComponent.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/en-us/windows/desktop/api/mmc/nf-mmc-iconsole-settoolbar">SetToolbar</a>
</td>
<td align="left" width="63%">
Used by instances of 
<a href="https://msdn.microsoft.com/65eaa5ef-182b-4fec-bb3d-a308ac9dc660">IComponent</a> only. Sets the toolbar interface to be used for this 
IComponent.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/en-us/windows/desktop/api/mmc/nf-mmc-iconsole-updateallviews">UpdateAllViews</a>
</td>
<td align="left" width="63%">
Generates a notification to update views because of content change.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/9a20d09d-219c-4bcb-95b3-67a44e41629e">IConsole2</a>



<a href="https://msdn.microsoft.com/be3d42a4-a18a-40a5-99fc-2cf2a848c564">IConsole3</a>



<a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a>



<a href="https://msdn.microsoft.com/c95742a4-ae9b-40f3-8d88-c4955e5a3032">MMC 2.0 Interfaces and Methods</a>
 

 

