---
UID: NS:tapi.linedialparams_tag
title: linedialparams_tag
author: windows-sdk-content
description: The LINEDIALPARAMS structure specifies a collection of dialing-related fields. Call the lineSetCallParams function or the TSPI_lineSetCallParams function to set parameters for a call using the LINEDIALPARAMS structure.
old-location: tapi2\linedialparams_str.htm
tech.root: TAPI
ms.assetid: efb65462-abe5-46db-9299-97871e0d011e
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: "*LPLINEDIALPARAMS, LINEDIALPARAMS, LINEDIALPARAMS structure [TAPI 2.2], LPLINEDIALPARAMS, LPLINEDIALPARAMS structure pointer [TAPI 2.2], _tapi2_linedialparams_str, linedialparams_tag, tapi/LINEDIALPARAMS, tapi/LPLINEDIALPARAMS, tapi2.linedialparams_str"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: tapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tapi.h
api_name:
 - LINEDIALPARAMS
product: Windows
targetos: Windows
req.typenames: LINEDIALPARAMS, *LPLINEDIALPARAMS
req.redist: 
---

# linedialparams_tag structure


## -description


The 
<b>LINEDIALPARAMS</b> structure specifies a collection of dialing-related fields. Call the 
<a href="https://msdn.microsoft.com/c8088116-2bfc-420f-a83a-d00c7947b6e7">lineSetCallParams</a> function or the 
<a href="https://msdn.microsoft.com/cc5d5347-ebb7-437a-a9a1-311b6c2a78ab">TSPI_lineSetCallParams</a> function to set parameters for a call using the 
<b>LINEDIALPARAMS</b> structure.


## -struct-fields




### -field dwDialPause

Duration of a comma in the dialable address, in milliseconds.


### -field dwDialSpeed

Interdigit time period between successive digits, in milliseconds.


### -field dwDigitDuration

Duration of a digit, in milliseconds.


### -field dwWaitForDialtone

Maximum amount of time to wait for a dial tone when a 'W' is used in the dialable address, in milliseconds.


## -remarks



This structure may not be extended.

If zero is specified for a member, the default value is used. If a nonzero value is specified for a member that is outside the range specified by the <b>MinDialParams</b> and <b>MaxDialParams</b> members in the 
<a href="https://msdn.microsoft.com/83e38453-bb93-4cc5-923f-d0cd2898350a">LINEDEVCAPS</a> structure, the nearest value within the valid range is used instead.

The 
<a href="https://msdn.microsoft.com/a7dc9cdc-3cc3-4b6a-98c8-e141402c781e">lineMakeCall</a> function allows an application to adjust the dialing parameters to be used for the call. The 
<a href="https://msdn.microsoft.com/c8088116-2bfc-420f-a83a-d00c7947b6e7">lineSetCallParams</a> function can be used to adjust the dialing parameters of an existing call. The 
<a href="https://msdn.microsoft.com/b077546b-cc95-44ce-99ee-f0007fd916b2">LINECALLINFO</a> structure lists the call's current dialing parameters.




## -see-also




<a href="https://msdn.microsoft.com/b077546b-cc95-44ce-99ee-f0007fd916b2">LINECALLINFO</a>



<a href="https://msdn.microsoft.com/83e38453-bb93-4cc5-923f-d0cd2898350a">LINEDEVCAPS</a>



<a href="https://msdn.microsoft.com/cc5d5347-ebb7-437a-a9a1-311b6c2a78ab">TSPI_lineSetCallParams</a>



<a href="https://msdn.microsoft.com/a7dc9cdc-3cc3-4b6a-98c8-e141402c781e">lineMakeCall</a>



<a href="https://msdn.microsoft.com/c8088116-2bfc-420f-a83a-d00c7947b6e7">lineSetCallParams</a>
 

 

