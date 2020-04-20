---
UID: NF:winfax.FaxCompleteJobParamsW
title: FaxCompleteJobParamsW function (winfax.h)
description: The FaxCompleteJobParams function creates both a FAX_COVERPAGE_INFO structure and a FAX_JOB_PARAM structure for a fax client application.helpviewer_keywords: ["FaxCompleteJobParams","FaxCompleteJobParams function [Fax Service]","FaxCompleteJobParamsA","FaxCompleteJobParamsW","_mfax_faxcompletejobparams","fax._mfax_faxcompletejobparams","winfax/FaxCompleteJobParams","winfax/FaxCompleteJobParamsA","winfax/FaxCompleteJobParamsW"]
old-location: fax\_mfax_faxcompletejobparams.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_9b8z.htm
ms.date: 12/05/2018
ms.keywords: FaxCompleteJobParams, FaxCompleteJobParams function [Fax Service], FaxCompleteJobParamsA, FaxCompleteJobParamsW, _mfax_faxcompletejobparams, fax._mfax_faxcompletejobparams, winfax/FaxCompleteJobParams, winfax/FaxCompleteJobParamsA, winfax/FaxCompleteJobParamsW
f1_keywords:
- winfax/FaxCompleteJobParams
dev_langs:
- c++
req.header: winfax.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FaxCompleteJobParamsW (Unicode) and FaxCompleteJobParamsA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WinFax.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- LibDef
api_location:
- WinFax.lib
- WinFax.dll
api_name:
- FaxCompleteJobParams
- FaxCompleteJobParamsA
- FaxCompleteJobParamsW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# FaxCompleteJobParamsW function


## -description


The FaxCompleteJobParams function creates both a <a href="https://docs.microsoft.com/windows/desktop/api/winfax/ns-winfax-fax_coverpage_infoa">FAX_COVERPAGE_INFO</a> structure and a <a href="https://docs.microsoft.com/windows/desktop/api/winfax/ns-winfax-fax_job_parama">FAX_JOB_PARAM</a> structure for a fax client application. This utility function supplies multiple members of these structures with values for the size of the structure, the sender's name, and optional billing code information.


## -parameters




### -param JobParams [in, out]

Type: <b>PFAX_JOB_PARAM*</b>

Pointer to the address of a buffer to contain a <a href="https://docs.microsoft.com/windows/desktop/api/winfax/ns-winfax-fax_job_parama">FAX_JOB_PARAM</a> structure. On output, this structure contains members with values that are available from the fax server.


### -param CoverpageInfo [in, out]

Type: <b>PFAX_COVERPAGE_INFO*</b>

Pointer to the address of a buffer to contain a <a href="https://docs.microsoft.com/windows/desktop/api/winfax/ns-winfax-fax_coverpage_infoa">FAX_COVERPAGE_INFO</a> structure. On output, this structure contains members with values that are available from the fax server.


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



The fax client application should call the <b>FaxCompleteJobParams</b> function before calling the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winfax/nf-winfax-faxsenddocumenta">FaxSendDocument</a> function. This enables the fax server to provide any values that are available for the members of the <a href="https://docs.microsoft.com/windows/desktop/api/winfax/ns-winfax-fax_job_parama">FAX_JOB_PARAM</a> and the <a href="https://docs.microsoft.com/windows/desktop/api/winfax/ns-winfax-fax_coverpage_infoa">FAX_COVERPAGE_INFO</a> structures. The application should not query the user's registry for this information because the location of the information can change. For more information, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-transmitting-faxes">Transmitting Faxes</a>.

The application must call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winfax/nc-winfax-pfaxfreebuffer">FaxFreeBuffer</a> function once to deallocate the buffer pointed to by the <i>JobParams</i> parameter, and again to deallocate the buffer pointed to by the <i>CoverpageInfo</i> parameter. For more information, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-freeing-fax-resources">Freeing Fax Resources</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winfax/ns-winfax-fax_coverpage_infoa">FAX_COVERPAGE_INFO</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winfax/ns-winfax-fax_job_parama">FAX_JOB_PARAM</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-functions">Fax Service Client API Functions</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winfax/nc-winfax-pfaxfreebuffer">FaxFreeBuffer</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winfax/nf-winfax-faxsenddocumenta">FaxSendDocument</a>
 

 

