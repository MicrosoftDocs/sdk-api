---
UID: NC:ras.RASADFUNCA
title: RASADFUNCA
author: windows-sdk-content
description: The RASADFunc function is an application-defined callback function that is used to provide a customized user interface for autodialing.
old-location: rras\rasadfunc.htm
old-project: RRAS
ms.assetid: e014624a-1ee1-4de3-ba59-cd090b3fa711
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: RASADFunc, RASADFunc callback, RASADFunc callback function [RAS], RASADFuncA, RASADFuncW, _ras_rasadfunc, ras/RASADFunc, ras/RASADFuncA, ras/RASADFuncW, rras.rasadfunc
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: ras.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RASADFuncW (Unicode) and RASADFuncA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: RSVP_STATUS_INFO, *LPRSVP_STATUS_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Ras.h
api_name:
 - RASADFunc
 - RASADFuncA
 - RASADFuncW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# RASADFUNCA callback function


## -description


The 
<b>RASADFunc</b> function is an application-defined callback function that is used to provide a customized user interface for autodialing.


## -parameters




### -param Arg1


### -param Arg2


### -param Arg3


### -param Arg4








#### - lpAutoDialParams [in]

Pointer to a 
<a href="https://msdn.microsoft.com/01ad65b0-20d0-4dc8-8856-6b9913f8dc29">RASADPARAMS</a> structure that indicates how to position the window of the AutoDial user interface. The structure can also specify a parent window for the AutoDial window.


#### - lpdwRetCode [out]

Pointer to a variable that receives a value if the function performs the dialing operation. If the dialing operation succeeds, set this variable to <b>ERROR_SUCCESS</b>. If the dialing operation fails, set it to a nonzero value.


#### - lpszEntry [in]

Pointer to a <b>null</b>-terminated string that specifies the phone-book entry to use.


#### - lpszPhonebook [in]

Pointer to a <b>null</b>-terminated string that specifies the full path and file name of a phone-book (PBK) file. If this parameter is <b>NULL</b>, the function uses the current default phone-book file. The default phone-book file is the one selected by the user in the <b>User Preferences</b> property sheet of the <b>Dial-Up Networking</b> dialog box. 




<b>Windows Me/98/95:  </b>This parameter is always <b>NULL</b>. Dial-up networking stores phone-book entries in the registry rather than in a phone-book file.


## -returns



If the application performs the dialing operation, return <b>TRUE</b>. Use the <i>lpdwRetCode</i> parameter to indicate the results of the dialing operation.

If the application does not perform the dialing operation, return <b>FALSE</b>. In this case, the system uses the default user interface for dialing.




## -remarks



When the system starts an AutoDial operation for a phone-book entry with a custom AutoDial handler, it calls the specified 
<b>RASADFunc</b>. The 
<b>RASADFunc</b> can start a thread to perform the custom-dialing operation. The 
<b>RASADFunc</b> function returns <b>TRUE</b> to indicate that it took over the dialing, or <b>FALSE</b> to allow the system to perform the dialing.

If the 
<b>RASADFunc</b> function performs the dialing operation, it presents its own user interface for dialing and calls the 
<a href="https://msdn.microsoft.com/579a9038-8216-4948-a065-fd45b97da73a">RasDial</a> function to do the actual dialing. The 
<b>RASADFunc</b> then returns <b>TRUE</b> to indicate that it took over the dialing. When the dialing operation has been completed, set the variable pointed to by the <i>lpdwRetCode</i> parameter to indicate success or failure.

The AutoDial DLL must provide both a <b>RASADFUNCA</b> (ANSI) and a <b>RASADFUNCW</b> (Unicode) version of the 
<b>RASADFunc</b> handler. To enable a 
<b>RASADFunc</b> AutoDial handler for a phone-book entry, use the 
<a href="https://msdn.microsoft.com/25c46850-4fb7-47a9-9645-139f0e869559">RASENTRY</a> structure in a call to the 
<a href="https://msdn.microsoft.com/6532b48b-0d80-4993-800e-c808bb7540d6">RasSetEntryProperties</a> function. The <b>szAutodialDll</b> member specifies the name of the DLL that contains the handler, and the <b>szAutodialFunc</b> member specifies the exported name of the handler. The <b>szAutodialFunc</b> member should not include the "A" or "W" suffix.

<b>RASADFunc</b> is a placeholder for the library-defined function name. The <b>RASADFUNC</b> type is a pointer to a 
<b>RASADFunc</b> function.




## -see-also




<a href="https://msdn.microsoft.com/25c46850-4fb7-47a9-9645-139f0e869559">RASENTRY</a>



<a href="https://msdn.microsoft.com/579a9038-8216-4948-a065-fd45b97da73a">RasDial</a>



<a href="https://msdn.microsoft.com/6532b48b-0d80-4993-800e-c808bb7540d6">RasSetEntryProperties</a>



<a href="https://msdn.microsoft.com/5016fa0b-72eb-484e-b8d7-af9de2e25689">Remote Access Service (RAS) Overview</a>



<a href="https://msdn.microsoft.com/5883a77a-6af8-47a8-bb28-6ef60a5aa2f1">Remote Access Service Functions</a>
 

 

