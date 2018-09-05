---
UID: NN:shobjidl.IEnumerableView
title: IEnumerableView
author: windows-sdk-content
description: Exposes methods that enumerate the contents of a view and receive notification from callback upon enumeration completion. This interface enables clients of a view to attempt to share the view's list of folder contents.
old-location: shell\IEnumerableView.htm
old-project: shell
ms.assetid: 6e096f7b-b40b-45ea-a348-ddfedf5913f8
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: IEnumerableView, IEnumerableView interface [Windows Shell], IEnumerableView interface [Windows Shell],described, _shell_IEnumerableView, shell.IEnumerableView, shobjidl/IEnumerableView
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shobjidl.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: VPWATERMARKFLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl.h
api_name:
 - IEnumerableView
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll
req.irql: 
req.product: Internet Explorer 6.01
---

# IEnumerableView interface


## -description


Exposes methods that enumerate the contents of a view and receive notification from callback upon enumeration completion. This interface enables clients of a view to attempt to share the view's list of folder contents.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumerableView</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumerableView</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumerableView</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/413d913d-e6f3-4e2d-bf1f-5d5ad6d4f650">CreateEnumIDListFromContents</a>
</td>
<td align="left" width="63%">
Creates an enumerator of ID lists from the contents of the view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/af824c16-5bbf-4c75-88d0-b76519152360">SetEnumReadyCallback</a>
</td>
<td align="left" width="63%">
Sets a callback on the view that is notified when the initial view enumeration is complete.

</td>
</tr>
</table> 


## -remarks




<a href="https://msdn.microsoft.com/3bc2615e-f07c-4959-b89e-bbbd2bf45a94">IFolderView</a> (a folder view) supports presentation of the contents of a folder, and exposes the <b>IEnumerableView</b> through <a href="_inet_IServiceProvider_QueryService_Method">QueryService</a> on service request SID_EnumerableView. <b>IEnumerableView</b> offers enhanced performance compared to obtaining the contents of the folder directly from the folder using <a href="https://msdn.microsoft.com/b6f139d3-c54c-4350-9d8b-cd534909a488">IEnumIDList</a> (call <a href="https://msdn.microsoft.com/248bec8b-0bf4-47d5-adb3-31a685a2c359">IShellFolder::EnumObjects</a> to return this interface). Since the view asked for the contents of the folder in order to display those contents, using <b>IEnumerableView</b> enables a client to get a copy of the work already done by <b>IFolderView</b>.

Typicallly, this enumeration service is compatible with most folders, and is only provided if it is safe to enumerate the contents of the view.  For example, using this service with a folder containing search results is not supported.
          



