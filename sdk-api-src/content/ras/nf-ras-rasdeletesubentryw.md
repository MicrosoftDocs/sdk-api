---
UID: NF:ras.RasDeleteSubEntryW
title: RasDeleteSubEntryW function (ras.h)
description: The RasDeleteSubEntry function deletes the specified subentry from the specified phone-book entry. (Unicode)
helpviewer_keywords: ["RasDeleteSubEntry", "RasDeleteSubEntry function [RAS]", "RasDeleteSubEntryW", "_ras_rasdeletesubentry", "ras/RasDeleteSubEntry", "ras/RasDeleteSubEntryW", "rras.rasdeletesubentry"]
old-location: rras\rasdeletesubentry.htm
tech.root: RRAS
ms.assetid: c423d0cc-7275-4703-abee-4eada625d956
ms.date: 12/05/2018
ms.keywords: RasDeleteSubEntry, RasDeleteSubEntry function [RAS], RasDeleteSubEntryA, RasDeleteSubEntryW, _ras_rasdeletesubentry, ras/RasDeleteSubEntry, ras/RasDeleteSubEntryA, ras/RasDeleteSubEntryW, rras.rasdeletesubentry
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RasDeleteSubEntryW
 - ras/RasDeleteSubEntryW
dev_langs:
 - c++
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

### -param dwSubEntryId [in]

Specifies the one-based index of the subentry.

## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is one of the following error codes or a value from <a href="/windows/desktop/RRAS/routing-and-remote-access-error-codes">Routing and Remote Access Error Codes</a> or Winerror.h.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)">RASENTRY</a>



<a href="/previous-versions/windows/desktop/legacy/aa377839(v=vs.85)">RASSUBENTRY</a>



<a href="/windows/desktop/api/ras/nf-ras-rasdeleteentrya">RasDeleteEntry</a>

## -remarks

> [!NOTE]
> The ras.h header defines RasDeleteSubEntry as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
