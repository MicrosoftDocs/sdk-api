---
UID: NF:appxpackaging.IAppxContentGroupsEnumerator.GetCurrent
title: IAppxContentGroupsEnumerator::GetCurrent
author: windows-sdk-content
description: Gets the content group at the current position of the enumerator.
old-location: appxpkg\iappxcontentgroupsenumerator_getcurrent.htm
old-project: appxpkg
ms.assetid: 1A7055F5-6121-4A3A-AE7C-4BFDF6D7F1A9
ms.author: windowssdkdev
ms.date: 06/22/2018
ms.keywords: GetCurrent, GetCurrent method [App packaging and management], GetCurrent method [App packaging and management],IAppxContentGroupsEnumerator interface, IAppxContentGroupsEnumerator interface [App packaging and management],GetCurrent method, IAppxContentGroupsEnumerator.GetCurrent, IAppxContentGroupsEnumerator::GetCurrent, appxpackaging/IAppxContentGroupsEnumerator::GetCurrent, appxpkg.iappxcontentgroupsenumerator_getcurrent
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: appxpackaging.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: AppxPackaging.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: APPX_PACKAGE_EDITOR_UPDATE_PACKAGE_OPTION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - AppxPackaging.h
api_name:
 - IAppxContentGroupsEnumerator.GetCurrent
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxContentGroupsEnumerator::GetCurrent


## -description


Gets the content group at the current position of the enumerator.


## -parameters




### -param stream [out, retval]

The current content group.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an error code that includes, but is not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_BOUNDS</b></dt>
</dl>
</td>
<td width="60%">
The enumerator has passed the last item in the collection.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/BA91A1A6-6C6B-4086-AE95-47372581429C">IAppxContentGroupsEnumerator</a>
 

 

