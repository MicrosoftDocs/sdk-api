---
UID: NF:comsvcs.GetObjectContext
title: GetObjectContext macro
author: windows-sdk-content
description: Retrieves a reference to the context that is associated with the current COM+ object.
old-location: cos\getobjectcontext.htm
old-project: cossdk
ms.assetid: e93406df-e61c-4ee5-9cd4-828aab2c05b6
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: GetObjectContext, GetObjectContext function [COM+], _cos_GetObjectContext, comsvcs/GetObjectContext, cos.getobjectcontext
ms.prod: windows
ms.technology: windows-sdk
ms.topic: macro
req.header: comsvcs.h
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
req.typenames: TRACKING_COLL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	ComSvcs.dll
api_name:
-	GetObjectContext
product: Windows
targetos: Windows
req.lib: ComSvcs.lib
req.dll: ComSvcs.dll
req.irql: 
---

# GetObjectContext macro


## -description


Retrieves a reference to the context that is associated with the current COM+ object.

For similar functionality, see <a href="https://msdn.microsoft.com/7e2edb2f-ca86-4636-aaad-7b00335065df">IMTxAS::GetObjectContext</a>.


## -parameters




### -param ppIOC

TBD






#### - ppInstanceContext [out]

A reference to <a href="https://msdn.microsoft.com/9395bc9a-dfe5-428a-839f-1c4ad090f636">IObjectContext</a> on the object's context. If the object's component has not been imported into an MTS package or if the <b>GetObjectContext</b> function is called from a constructor or an <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> method, this parameter is set to a <b>NULL</b> pointer.


## -remarks



An object's context is not accessible from an object's constructor or from any <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> method.

An object should never attempt to pass its <a href="https://msdn.microsoft.com/9395bc9a-dfe5-428a-839f-1c4ad090f636">IObjectContext</a> reference to another object. If you pass an <b>IObjectContext</b> reference to another object, it is no longer a valid reference.

When an object obtains a reference to its <a href="https://msdn.microsoft.com/9395bc9a-dfe5-428a-839f-1c4ad090f636">IObjectContext</a>, it must release the <b>IObjectContext</b> object when it is finished with it.




## -see-also




<a href="https://msdn.microsoft.com/50ccf75e-2652-4254-a771-af83cc9248b3">COM+ Contexts and Threading Models</a>



<a href="https://msdn.microsoft.com/7e2edb2f-ca86-4636-aaad-7b00335065df">IMTxAS::GetObjectContext</a>



<a href="https://msdn.microsoft.com/9395bc9a-dfe5-428a-839f-1c4ad090f636">IObjectContext</a>
 

 

