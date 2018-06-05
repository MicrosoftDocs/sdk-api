---
UID: NF:tuner.IATSCComponentType.put_Flags
title: IATSCComponentType::put_Flags
author: windows-sdk-content
description: The put_Flags method specifies whether an audio component is in AC-3 format.
old-location: mstv\iatsccomponenttype_put_flags.htm
old-project: mstv
ms.assetid: e2959a4c-70a8-43a4-8bc5-4bfc965e8085
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IATSCComponentType interface [Microsoft TV Technologies],put_Flags method, IATSCComponentType.put_Flags, IATSCComponentType::put_Flags, IATSCComponentTypeput_Flags, mstv.iatsccomponenttype_put_flags, put_Flags, put_Flags method [Microsoft TV Technologies], put_Flags method [Microsoft TV Technologies],IATSCComponentType interface, tuner/IATSCComponentType::put_Flags
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	tuner.h
api_name:
-	IATSCComponentType.put_Flags
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IATSCComponentType::put_Flags


## -description



The <b>put_Flags</b> method specifies whether an audio component is in AC-3 format.




## -parameters




### -param flags






#### - Flags [in]

Specifies one of the following values:

<table>
<tr>
<th>
                  Value
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>Zero</td>
<td>The component does not contain AC-3 audio</td>
</tr>
<tr>
<td>ATSCCT_AC3</td>
<td>The component contains AC-3 audio</td>
</tr>
</table>
 

See <a href="https://msdn.microsoft.com/fd4db1f7-7c32-4fcc-b95a-269a550311ef">ATSCComponentTypeFlags Enumeration</a>.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/c7e05f63-b2cf-4a99-8e0f-bc7ec00463cf">IATSCComponentType Interface</a>
 

 

