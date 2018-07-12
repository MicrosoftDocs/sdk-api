---
UID: NF:bits3_0.IBackgroundCopyJob4.GetOwnerElevationState
title: IBackgroundCopyJob4::GetOwnerElevationState
author: windows-sdk-content
description: Gets a value that determines if the token of the owner was elevated at the time they created or took ownership of the job.
old-location: bits\ibackgroundcopyjob4_getownerelevationstate.htm
old-project: bits
ms.assetid: 2ab62c27-5ba1-46f3-a5e9-020fde17a1ef
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: GetOwnerElevationState, GetOwnerElevationState method [BITS], GetOwnerElevationState method [BITS],IBackgroundCopyJob4 interface, IBackgroundCopyJob4 interface [BITS],GetOwnerElevationState method, IBackgroundCopyJob4.GetOwnerElevationState, IBackgroundCopyJob4::GetOwnerElevationState, bits.ibackgroundcopyjob4_getownerelevationstate, bits3_0/IBackgroundCopyJob4::GetOwnerElevationState
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: bits3_0.h
req.include-header: Bits.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits3_0.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: BG_CERT_STORE_LOCATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Bits.lib
 - Bits.dll
api_name:
 - IBackgroundCopyJob4.GetOwnerElevationState
product: Windows
targetos: Windows
req.lib: Bits.lib
req.dll: 
req.irql: 
---

# IBackgroundCopyJob4::GetOwnerElevationState


## -description


Gets a value that determines if the token of the owner was elevated at the time they created or took ownership of the job.


## -parameters




### -param pElevated [out]

Is <b>TRUE</b> if the token of the owner was elevated at the time they created or took ownership of the job; otherwise, <b>FALSE</b>.


## -returns



The method returns the following return values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success

</td>
</tr>
</table>
 




## -remarks



For details on elevated tokens, see <a href="https://msdn.microsoft.com/02439ab3-b885-4a2f-b507-0c48d2b30b76">User Account Control and BITS</a>.

Note that if the job was created with an elevated token, all subsequent updates to the job must be done with an elevated token.




## -see-also




<a href="https://msdn.microsoft.com/68909710-f749-487e-b064-9f8630929c53">IBackgroundCopyJob4</a>
 

 

