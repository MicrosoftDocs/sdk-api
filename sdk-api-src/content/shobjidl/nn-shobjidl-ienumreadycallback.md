---
UID: NN:shobjidl.IEnumReadyCallback
title: IEnumReadyCallback
author: windows-sdk-content
description: Exposes methods that enable the view to notify the implementer when the enumeration has completed.
old-location: shell\IEnumReadyCallback.htm
old-project: shell
ms.assetid: 6c36e13d-9bd8-4ec1-980a-dc4ebd4dbcd9
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IEnumReadyCallback, IEnumReadyCallback interface [Windows Shell], IEnumReadyCallback interface [Windows Shell],described, _shell_IEnumReadyCallback, shell.IEnumReadyCallback, shobjidl/IEnumReadyCallback
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
 - IEnumReadyCallback
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll
req.irql: 
req.product: Internet Explorer 6.01
---

# IEnumReadyCallback interface


## -description


Exposes methods that enable the view to notify the implementer when the enumeration has completed.  The view calls this method to tell the implementer that the enumeration can be retrieved via <a href="https://msdn.microsoft.com/413d913d-e6f3-4e2d-bf1f-5d5ad6d4f650">IEnumerableView::CreateEnumIDListFromContents</a>.  The callback allows the implementer to share the views enumeration.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumReadyCallback</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumReadyCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumReadyCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4bb0772a-a863-49eb-a262-755d0ea3ea86">EnumReady</a>
</td>
<td align="left" width="63%">
Notifies the implementer that the view's item enumeration has completed.  This callback interface is provided to the view via <a href="https://msdn.microsoft.com/af824c16-5bbf-4c75-88d0-b76519152360">IEnumerableView::SetEnumReadyCallback</a>


</td>
</tr>
</table> 

