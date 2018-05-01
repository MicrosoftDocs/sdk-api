---
UID: NF:wiamdef.wiasParseEndorserString
title: wiasParseEndorserString function
author: windows-driver-content
description: The wiasParseEndorserString function parses an endorser string, replacing WIA service-defined and vendor-defined tokens in the string with values associated with those tokens.
old-location: image\wiasparseendorserstring.htm
old-project: image
ms.assetid: c724a4f5-55ef-413d-bd1a-9cd39d3e42f5
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: image.wiasparseendorserstring, wiamdef/wiasParseEndorserString, wiasFncs_09a845d0-52f1-4985-baf6-2cb2676fad3e.xml, wiasParseEndorserString, wiasParseEndorserString function [Imaging Devices]
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wiamdef.h
req.include-header: Wiamdef.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Microsoft Windows Me and in Windows XP and later versions of the Windows operating systems.
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
req.typenames: WER_RUNTIME_EXCEPTION_INFORMATION, *PWER_RUNTIME_EXCEPTION_INFORMATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Wiaservc.dll
api_name:
-	wiasParseEndorserString
product: Windows
targetos: Windows
req.lib: Wiaservc.lib
req.dll: Wiaservc.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# wiasParseEndorserString function


## -description


The <b>wiasParseEndorserString</b> function parses an endorser string, replacing WIA service-defined and vendor-defined tokens in the string with values associated with those tokens.


## -parameters




### -param pWiasContext [in]

Pointer to a WIA Item context (the context of the item containing the WIA_DPS_ENDORSER_STRING property (described in the Microsoft Windows SDK documentation)).


### -param lFlags

Reserved for system use and should be set to 0.


### -param pInfo [out, optional]

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff549556">WIAS_ENDORSER_INFO</a> structure containing the page count and a list of custom token/value pairs. Can be <b>NULL</b>.


### -param pOutputString [out]

Pointer to a memory location that receives the address of the parsed endorser string. If *<i>pOutputString</i> is non-<b>NULL</b> on entry, then the function assumes that the caller allocated the buffer; otherwise the WIA service will allocate it. Note that the WIA service assumes the <i>maximum</i> resultant endorser string is MAX_PATH (defined in <i>stdlib.h</i>) characters long. If the driver expects the string to be longer, it should allocate the buffer itself. If the caller allocates the buffer, it <i>must</i> initialize the contents of the buffer to zero before using this function.


## -returns



On success, the function returns S_OK. If the function fails, it returns a standard COM error or one of the WIA_ERROR_XXX errors (described in the Windows SDK documentation).




## -remarks



An application sets the WIA_DPS_ENDORSER_STRING property to a string that can contain the WIA service-defined tokens $DATE$, $TIME$, $PAGE_COUNT$, $DAY$, $MONTH$, and $YEAR$, as well as vendor-defined tokens. After a driver calls <b>wiasParseEndorserString</b>, the string pointed to by <i>pOutputString</i> contains a copy of the string in WIA_DPS_ENDORSER_STRING property, but with any tokens replaced by the values the tokens represent. For example, if the application set the endorser string to "This page was scanned on $DATE$", and the current date was October 1, 2000, the resulting output string would be "This page was scanned on 2000/10/1".

The list of standard WIA endorser tokens can be found in <i>wiadef.h</i>.

Drivers can request that <b>wiasParseEndorserString</b> substitute values for vendor-defined tokens by filling out a <a href="https://msdn.microsoft.com/library/windows/hardware/ff549562">WIAS_ENDORSER_VALUE</a> structure for each token/value pair, and packaging all of these structures in a <a href="https://msdn.microsoft.com/library/windows/hardware/ff549556">WIAS_ENDORSER_INFO</a> structure. The following example shows how this function can be used.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>HRESULT hr  = S_OK;
BSTR  bstrResultingEndorser   = NULL;
WIAS_ENDORSER_VALUE  aMyTokens[] = {L"$MY_TOKEN$", L"My value"};
WIAS_ENDORSER_INFO  Info     = {0, 1, aMyTokens};
hr = wiasParseEndorserString(pWiasContext, 0, 
                             &amp;Info, &amp;bstrResultingEndorser);</pre>
</td>
</tr>
</table></span></div>
Assuming that the WIA_DPS_ENDORSER_STRING property contains "This is $MY_TOKEN$", and that the call to <b>wiasParseEndorserString</b> was successful, <i>bstrResultingEndorser</i> will now contain "This is My value".




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff549556">WIAS_ENDORSER_INFO</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549562">WIAS_ENDORSER_VALUE</a>
 

 

