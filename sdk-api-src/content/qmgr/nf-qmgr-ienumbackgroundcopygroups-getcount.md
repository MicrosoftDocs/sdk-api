---
UID: NF:qmgr.IEnumBackgroundCopyGroups.GetCount
title: IEnumBackgroundCopyGroups::GetCount
author: windows-driver-content
description: Use the GetCount method to retrieve a count of the number of groups in the enumeration.
old-location: bits\ienumbackgroundcopygroups_getcount.htm
old-project: Bits
ms.assetid: 70bbc495-f133-4703-a51a-1a1a180720f4
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: GetCount, GetCount method [BITS], GetCount method [BITS],IEnumBackgroundCopyGroups interface, IEnumBackgroundCopyGroups interface [BITS],GetCount method, IEnumBackgroundCopyGroups.GetCount, IEnumBackgroundCopyGroups::GetCount, bits.ienumbackgroundcopygroups_getcount, qmgr/IEnumBackgroundCopyGroups::GetCount
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: qmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Qmgr.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: GROUPPROP
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	QmgrPrxy.dll
api_name:
-	IEnumBackgroundCopyGroups.GetCount
product: Windows
targetos: Windows
req.lib: 
req.dll: QmgrPrxy.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IEnumBackgroundCopyGroups::GetCount


## -description


<p class="CCE_Message">[<b>IEnumBackgroundCopyGroups</b> is available for use in the operating systems specified in the Requirements section.  It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/72668c9b-e6f3-4f3f-9d4b-50d930d1889d">BITS interfaces</a>.]

Use the <b>GetCount</b> method to retrieve a count of the number of groups in the enumeration.


## -parameters




### -param puCount [out]

Number of groups in the enumeration.


## -returns



This method returns <b>S_OK</b> on success.




## -see-also




<a href="https://msdn.microsoft.com/64a05103-9749-41fd-9987-8bb17b9284f7">IEnumBackgroundCopyGroups</a>
 

 

