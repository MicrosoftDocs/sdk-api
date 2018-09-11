---
UID: NF:tapi.lineSetTollList
title: lineSetTollList function
author: windows-sdk-content
description: The lineSetTollList function manipulates the toll list.
old-location: tapi2\linesettolllist.htm
tech.root: tapi
ms.assetid: 40471e45-cb1d-4730-ba35-ffec99953235
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: "_tapi2_linesettolllist, lineSetTollList, lineSetTollList function [TAPI 2.2], lineSetTollListA, lineSetTollListW, tapi/lineSetTollList, tapi/lineSetTollListA, tapi/lineSetTollListW, tapi2.linesettolllist"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: tapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: lineSetTollListW (Unicode) and lineSetTollListA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Tapi32.dll
api_name:
 - lineSetTollList
 - lineSetTollListA
 - lineSetTollListW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# lineSetTollList function


## -description


The 
<b>lineSetTollList</b> function manipulates the toll list.


## -parameters




### -param hLineApp

Application handle returned by 
<a href="https://msdn.microsoft.com/18cd145d-e434-433a-ab10-91bf5b060c21">lineInitializeEx</a>. If an application has not yet called the 
<b>lineInitializeEx</b> function, it can set the <i>hLineApp</i> parameter to zero.


### -param dwDeviceID

Device identifier for the line device upon which the call is intended to be dialed, so that variations in dialing procedures on different lines can be applied to the translation process.


### -param lpszAddressIn

Pointer to a <b>null</b>-terminated string containing the address from which the prefix information is to be extracted for processing. This parameter must not be <b>NULL</b>, and it must be in the canonical address format.


### -param dwTollListOption

Toll list operation to be performed. This parameter uses one and only one of the 
<a href="https://msdn.microsoft.com/22878045-c1d1-45b6-a864-d979514e4b7d">LINETOLLLISTOPTION_ Constants</a>.


## -returns



Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

LINEERR_BADDEVICEID, LINEERR_NODRIVER, LINEERR_INVALAPPHANDLE, LINEERR_NOMEM, LINEERR_INVALADDRESS, LINEERR_OPERATIONFAILED, LINEERR_INVALPARAM, LINEERR_RESOURCEUNAVAIL, LINEERR_INIFILECORRUPT, LINEERR_UNINITIALIZED, LINEERR_INVALLOCATION.




## -see-also




<a href="https://msdn.microsoft.com/09d10789-bc36-47c7-b77d-8698ae75541a">Basic Telephony Services Reference</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>



<a href="https://msdn.microsoft.com/18cd145d-e434-433a-ab10-91bf5b060c21">lineInitializeEx</a>
 

 

