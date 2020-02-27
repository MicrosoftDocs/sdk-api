---
UID: NF:qmgr.IEnumBackgroundCopyGroups.GetCount
title: IEnumBackgroundCopyGroups::GetCount (qmgr.h)
description: Use the GetCount method to retrieve a count of the number of groups in the enumeration.
old-location: bits\ienumbackgroundcopygroups_getcount.htm
tech.root: Bits
ms.assetid: 70bbc495-f133-4703-a51a-1a1a180720f4
ms.date: 12/05/2018
ms.keywords: GetCount, GetCount method [BITS], GetCount method [BITS],IEnumBackgroundCopyGroups interface, IEnumBackgroundCopyGroups interface [BITS],GetCount method, IEnumBackgroundCopyGroups.GetCount, IEnumBackgroundCopyGroups::GetCount, bits.ienumbackgroundcopygroups_getcount, qmgr/IEnumBackgroundCopyGroups::GetCount
f1_keywords:
- qmgr/IEnumBackgroundCopyGroups.GetCount
dev_langs:
- c++
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
req.lib: 
req.dll: QmgrPrxy.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- QmgrPrxy.dll
api_name:
- IEnumBackgroundCopyGroups.GetCount
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumBackgroundCopyGroups::GetCount


## -description


<p class="CCE_Message">[<b>IEnumBackgroundCopyGroups</b> is available for use in the operating systems specified in the Requirements section.  It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://docs.microsoft.com/windows/desktop/Bits/bits-interfaces">BITS interfaces</a>.]

Use the <b>GetCount</b> method to retrieve a count of the number of groups in the enumeration.


## -parameters




### -param puCount [out]

Number of groups in the enumeration.


## -returns



This method returns <b>S_OK</b> on success.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/qmgr/nn-qmgr-ienumbackgroundcopygroups">IEnumBackgroundCopyGroups</a>
 

 

