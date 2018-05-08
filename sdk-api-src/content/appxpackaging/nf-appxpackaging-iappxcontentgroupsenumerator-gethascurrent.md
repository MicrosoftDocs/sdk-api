---
UID: NF:appxpackaging.IAppxContentGroupsEnumerator.GetHasCurrent
title: IAppxContentGroupsEnumerator::GetHasCurrent
author: windows-driver-content
description: Determines whether there is a content group at the current position of the enumerator.
old-location: appxpkg\iappxcontentgroupsenumerator_gethascurrent.htm
old-project: appxpkg
ms.assetid: 5935EA6A-AD7F-4462-B539-A01439D0A373
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetHasCurrent, GetHasCurrent method [App packaging and management], GetHasCurrent method [App packaging and management],IAppxContentGroupsEnumerator interface, IAppxContentGroupsEnumerator interface [App packaging and management],GetHasCurrent method, IAppxContentGroupsEnumerator.GetHasCurrent, IAppxContentGroupsEnumerator::GetHasCurrent, appxpackaging/IAppxContentGroupsEnumerator::GetHasCurrent, appxpkg.iappxcontentgroupsenumerator_gethascurrent
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: APPX_PACKAGE_EDITOR_UPDATE_PACKAGE_OPTION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	AppxPackaging.h
api_name:
-	IAppxContentGroupsEnumerator.GetHasCurrent
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxContentGroupsEnumerator::GetHasCurrent


## -description


Determines whether there is a content group at the current position of the enumerator.


## -parameters




### -param hasCurrent [out, retval]

<b>TRUE</b> if the enumerator's current position references an item; <b>FALSE</b> if the enumerator has passed the last item in the collection.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/BA91A1A6-6C6B-4086-AE95-47372581429C">IAppxContentGroupsEnumerator</a>
 

 

