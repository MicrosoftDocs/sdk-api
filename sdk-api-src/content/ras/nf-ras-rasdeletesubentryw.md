---
UID: NF:ras.RasDeleteSubEntryW
title: RasDeleteSubEntryW function
author: windows-sdk-content
description: The RasDeleteSubEntry function deletes the specified subentry from the specified phone-book entry.
old-location: rras\rasdeletesubentry.htm
tech.root: rras
ms.assetid: c423d0cc-7275-4703-abee-4eada625d956
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: RasDeleteSubEntry, RasDeleteSubEntry function [RAS], RasDeleteSubEntryA, RasDeleteSubEntryW, _ras_rasdeletesubentry, ras/RasDeleteSubEntry, ras/RasDeleteSubEntryA, ras/RasDeleteSubEntryW, rras.rasdeletesubentry
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ras.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RasDeleteSubEntryW (Unicode) and RasDeleteSubEntryA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Rasapi32.lib
req.dll: Rasapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rasapi32.dll
api_name:
 - RasDeleteSubEntry
 - RasDeleteSubEntryA
 - RasDeleteSubEntryW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RasDeleteSubEntryW function


## -description


The 
<b>RasDeleteSubEntry</b> function deletes the specified subentry from the specified phone-book entry.


## -parameters




### -param pszPhonebook [in]

Pointer to a <b>null</b>-terminated string that specifies the full path and file name of a phone-book (PBK) file. If this parameter is <b>NULL</b>, the function uses the current default phone-book file.


### -param pszEntry [in]

Pointer to a <b>null</b>-terminated string that contains the name of an existing entry from which a subentry is to be deleted.


#### - dwSubEntryId [in]

Specifies the one-based index of the subentry.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is one of the following error codes or a value from <a href="https://msdn.microsoft.com/1fa41438-7c93-4e9c-851c-652fba23da4f">Routing and Remote Access Error Codes</a> or Winerror.h.




## -see-also




<a href="https://msdn.microsoft.com/25c46850-4fb7-47a9-9645-139f0e869559">RASENTRY</a>



<a href="https://msdn.microsoft.com/48c1b100-e490-41a0-8324-6be2297bd814">RASSUBENTRY</a>



<a href="https://msdn.microsoft.com/80a6c2d3-917b-4d13-867f-a1399d434105">RasDeleteEntry</a>
 

 

