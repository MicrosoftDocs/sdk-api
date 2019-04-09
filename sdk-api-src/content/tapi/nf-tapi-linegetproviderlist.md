---
UID: NF:tapi.lineGetProviderList
title: lineGetProviderList function (tapi.h)
author: windows-sdk-content
description: The lineGetProviderList function returns a list of service providers currently installed in the telephony system.
old-location: tapi2\linegetproviderlist.htm
tech.root: Tapi
ms.assetid: 87d43409-e8c5-401a-87a2-02568ed0af4a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "_tapi2_linegetproviderlist, lineGetProviderList, lineGetProviderList function [TAPI 2.2], lineGetProviderListA, lineGetProviderListW, tapi/lineGetProviderList, tapi/lineGetProviderListA, tapi/lineGetProviderListW, tapi2.linegetproviderlist"
ms.topic: function
req.header: tapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: lineGetProviderListW (Unicode) and lineGetProviderListA (ANSI)
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
 - lineGetProviderList
 - lineGetProviderListA
 - lineGetProviderListW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# lineGetProviderList function


## -description


The 
<b>lineGetProviderList</b> function returns a list of service providers currently installed in the telephony system.


## -parameters




### -param dwAPIVersion

Highest version of TAPI supported by the application (not necessarily the value negotiated by 
<a href="https://msdn.microsoft.com/71eb55de-281b-42a9-8d9b-7ded62cb006a">lineNegotiateAPIVersion</a> on some particular line device).


### -param lpProviderList

Pointer to a memory location where TAPI can return a 
<a href="https://msdn.microsoft.com/75790ffd-bb1b-4efc-a905-5727d31f8aec">LINEPROVIDERLIST</a> structure. Prior to calling 
<b>lineGetProviderList</b>, the application must set the <b>dwTotalSize</b> member of this structure to indicate the amount of memory available to TAPI for returning information. 




<div class="alert"><b>Note</b>  If the size parameters in the structure are not correct, there is a possibility that data could get overwritten. For more information on setting structure sizes, see the 
<a href="https://msdn.microsoft.com/61313fe3-74a1-4195-b5af-37463dad02c1">memory allocation</a> topic. </div>
<div> </div>

## -returns



Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

LINEERR_INCOMPATIBLEAPIVERSION, LINEERR_NOMEM, LINEERR_INIFILECORRUPT, LINEERR_OPERATIONFAILED, LINEERR_INVALPOINTER, LINEERR_STRUCTURETOOSMALL.




## -see-also




<a href="https://msdn.microsoft.com/75790ffd-bb1b-4efc-a905-5727d31f8aec">LINEPROVIDERLIST</a>



<a href="https://msdn.microsoft.com/d4338b3c-cd84-4abb-b74e-9df895c8355b">Supplementary Line Service Functions</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>



<a href="https://msdn.microsoft.com/71eb55de-281b-42a9-8d9b-7ded62cb006a">lineNegotiateAPIVersion</a>
 

 

