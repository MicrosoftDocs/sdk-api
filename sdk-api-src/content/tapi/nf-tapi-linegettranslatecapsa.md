---
UID: NF:tapi.lineGetTranslateCapsA
title: lineGetTranslateCapsA function
author: windows-sdk-content
description: The lineGetTranslateCaps function returns address translation capabilities.
old-location: tapi2\linegettranslatecaps.htm
tech.root: tapi
ms.assetid: 77437b06-fb02-44b5-8642-b3de700853ef
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "_tapi2_linegettranslatecaps, lineGetTranslateCaps, lineGetTranslateCaps function [TAPI 2.2], lineGetTranslateCapsA, lineGetTranslateCapsW, tapi/lineGetTranslateCaps, tapi/lineGetTranslateCapsA, tapi/lineGetTranslateCapsW, tapi2.linegettranslatecaps"
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
req.unicode-ansi: lineGetTranslateCapsW (Unicode) and lineGetTranslateCapsA (ANSI)
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
 - lineGetTranslateCaps
 - lineGetTranslateCapsA
 - lineGetTranslateCapsW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# lineGetTranslateCapsA function


## -description


The 
<b>lineGetTranslateCaps</b> function returns address translation capabilities.


## -parameters




### -param hLineApp

Handle returned by the 
<a href="https://msdn.microsoft.com/18cd145d-e434-433a-ab10-91bf5b060c21">lineInitializeEx</a> function. If an application has not yet called the 
<b>lineInitializeEx</b> function, this parameter can be zero.

<div class="alert"><b>Note</b>   TAPI 1.4 applications must set this parameter to a valid hLineApp handle, as returned by the <a href="https://msdn.microsoft.com/4b406f19-be9b-4130-91a7-5fdfa56f7fc3">lineInitialize</a> function.

</div>
<div> </div>

### -param dwAPIVersion

Highest version of TAPI supported by the application (not necessarily the value negotiated by 
<a href="https://msdn.microsoft.com/71eb55de-281b-42a9-8d9b-7ded62cb006a">lineNegotiateAPIVersion</a> on some particular line device).


### -param lpTranslateCaps

Pointer to a location to which a 
<a href="https://msdn.microsoft.com/9b4dcbe6-41e9-4b9c-9150-d0c7edef5a19">LINETRANSLATECAPS</a> structure is loaded. Prior to calling 
<b>lineGetTranslateCaps</b>, the application must  set the <b>dwTotalSize</b> member of this structure to indicate the amount of memory available to TAPI for returning information. 




<div class="alert"><b>Note</b>  If the size parameters in the structure are not correct, there is a possibility that data could get overwritten. For more information on setting structure sizes, see the 
<a href="https://msdn.microsoft.com/61313fe3-74a1-4195-b5af-37463dad02c1">memory allocation</a> topic.</div>
<div> </div>

## -returns



Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

LINEERR_INCOMPATIBLEAPIVERSION, LINEERR_NOMEM, LINEERR_INIFILECORRUPT, LINEERR_OPERATIONFAILED, LINEERR_INVALAPPHANDLE, LINEERR_RESOURCEUNAVAIL, LINEERR_INVALPOINTER, LINEERR_STRUCTURETOOSMALL, LINEERR_NODRIVER.




## -see-also




<a href="https://msdn.microsoft.com/09d10789-bc36-47c7-b77d-8698ae75541a">Basic Telephony Services Reference</a>



<a href="https://msdn.microsoft.com/9b4dcbe6-41e9-4b9c-9150-d0c7edef5a19">LINETRANSLATECAPS</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>



<a href="https://msdn.microsoft.com/18cd145d-e434-433a-ab10-91bf5b060c21">lineInitializeEx</a>



<a href="https://msdn.microsoft.com/71eb55de-281b-42a9-8d9b-7ded62cb006a">lineNegotiateAPIVersion</a>
 

 

