---
UID: NN:mmc.IConsole
title: IConsole
author: windows-sdk-content
description: Enables communication with the console.
old-location: mmc\iconsole.htm
old-project: MMC
ms.assetid: 65154EB1-ABE5-4C4F-8B09-08633D82FD62
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: IConsole, IConsole interface [MMC], IConsole interface [MMC],described, mmc.iconsole, mmc/IConsole
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MMC_VIEW_TYPE
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
req.lib: 
req.dll: Mmcndmgr.dll
req.irql: 
req.product: GDI+ 1.1
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
<a href="https://msdn.microsoft.com/46eb727b-cc7f-42d9-8fc7-33195e4228a8">GetMainWindow</a>
</td>
<td align="left" width="63%">
Returns a handle to the main frame window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cdb9b389-0882-4e39-976e-cbbb1782edbb">MessageBox</a>
</td>
<td align="left" width="63%">
Displays a message box.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/44d81680-74ed-4a64-843b-feda6851a99e">NewWindow</a>
</td>
<td align="left" width="63%">
Creates a new window rooted at the specified scope item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9ea9f220-6e98-45c1-91aa-5af3f12d560e">QueryConsoleVerb</a>
</td>
<td align="left" width="63%">
Query for the 
<a href="https://msdn.microsoft.com/9c4338c1-eb5e-47f3-8b5b-0623690bd5f6">IConsoleVerb</a> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/770f1fea-24e7-421f-8792-e958178be1ea">QueryResultImageList</a>
</td>
<td align="left" width="63%">
Queries the console-provided result pane's image list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7736919a-ca02-4dda-a475-685a1b306422">QueryResultView</a>
</td>
<td align="left" width="63%">
Queries IConsole for the result view object's <a href="_com_iunknown">IUnknown</a> interface pointer.

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
<a href="https://msdn.microsoft.com/43d6ea1a-6ba4-4566-8bf7-3763f3a54f8d">SelectScopeItem</a>
</td>
<td align="left" width="63%">
Selects the given scope item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8677d851-5cc3-4518-930d-d4b5b390ffd4">SetHeader</a>
</td>
<td align="left" width="63%">
Used by instances of 
<a href="https://msdn.microsoft.com/65eaa5ef-182b-4fec-bb3d-a308ac9dc660">IComponent</a> only. Sets the header interface to be used for this 
IComponent.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a1858634-ac5b-42f3-a8cb-cdc269e771d8">SetToolbar</a>
</td>
<td align="left" width="63%">
Used by instances of 
<a href="https://msdn.microsoft.com/65eaa5ef-182b-4fec-bb3d-a308ac9dc660">IComponent</a> only. Sets the toolbar interface to be used for this 
IComponent.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/766c63ca-fe91-4c24-a118-352dc55f16e4">UpdateAllViews</a>
</td>
<td align="left" width="63%">
Generates a notification to update views because of content change.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/9a20d09d-219c-4bcb-95b3-67a44e41629e">IConsole2</a>



<a href="https://msdn.microsoft.com/be3d42a4-a18a-40a5-99fc-2cf2a848c564">IConsole3</a>



<a href="_com_iunknown">IUnknown</a>



<a href="https://msdn.microsoft.com/c95742a4-ae9b-40f3-8d88-c4955e5a3032">MMC 2.0 Interfaces and Methods</a>
 

 

