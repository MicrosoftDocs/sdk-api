---
UID: NF:msiquery.MsiSummaryInfoGetPropertyW
title: MsiSummaryInfoGetPropertyW function (msiquery.h)
description: The MsiSummaryInfoGetProperty function gets a single property from the summary information stream. (Unicode)
helpviewer_keywords: ["MsiSummaryInfoGetProperty", "MsiSummaryInfoGetProperty function", "MsiSummaryInfoGetPropertyW", "_msi_msisummaryinfogetproperty", "msiquery/MsiSummaryInfoGetProperty", "msiquery/MsiSummaryInfoGetPropertyW", "setup.msisummaryinfogetproperty"]
old-location: setup\msisummaryinfogetproperty.htm
tech.root: setup
ms.assetid: 7df4bd31-85a7-4b61-beaf-5c1f2117e6f5
ms.date: 12/05/2018
ms.keywords: MsiSummaryInfoGetProperty, MsiSummaryInfoGetProperty function, MsiSummaryInfoGetPropertyA, MsiSummaryInfoGetPropertyW, _msi_msisummaryinfogetproperty, msiquery/MsiSummaryInfoGetProperty, msiquery/MsiSummaryInfoGetPropertyA, msiquery/MsiSummaryInfoGetPropertyW, setup.msisummaryinfogetproperty
req.header: msiquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiSummaryInfoGetPropertyW (Unicode) and MsiSummaryInfoGetPropertyA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MsiSummaryInfoGetPropertyW
 - msiquery/MsiSummaryInfoGetPropertyW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msi.dll
 - Ext-MS-Win-MSI-Misc-l1-1-0.dll
api_name:
 - MsiSummaryInfoGetProperty
 - MsiSummaryInfoGetPropertyA
 - MsiSummaryInfoGetPropertyW
---

# MsiSummaryInfoGetPropertyW function


## -description

The 
<b>MsiSummaryInfoGetProperty</b> function gets a single property from the <a href="/windows/desktop/Msi/summary-information-stream">summary information stream</a>.


<div class="alert"><b>Note</b>  The meaning of the property value depends on whether the summary information stream is for an installation database (.msi file), transform (.mst file) or patch (.msp file). See <a href="/windows/desktop/Msi/summary-property-descriptions">Summary Property Descriptions</a> and <a href="/windows/desktop/Msi/summary-information-stream-property-set">Summary Information Stream Property Set</a> for more information about summary information properties.</div>
<div> </div>

## -parameters

### -param hSummaryInfo [in]

Handle to summary information.

### -param uiProperty [in]

Specifies the property ID of the summary property. This parameter can be a property ID  listed in the <a href="/windows/desktop/Msi/summary-information-stream-property-set">Summary Information Stream Property Set</a>.  This function does not return values for PID_DICTIONARY OR PID_THUMBNAIL property.

### -param puiDataType [out]

Receives the returned property type. This  parameter can be a type listed in the  
<a href="/windows/desktop/Msi/summary-information-stream-property-set">Summary Information Stream Property Set</a>.

### -param piValue [out]

Receives the returned integer property data.

### -param pftValue [out]

Pointer to a file value.

### -param szValueBuf [out]

Pointer to the buffer that receives the null terminated summary information property value. Do not attempt to determine the size of the buffer by passing in a null (value=0) for <i>szValueBuf</i>. You can get the size of the buffer by passing in an empty string (for example ""). The function then returns ERROR_MORE_DATA and <i>pcchValueBuf</i> contains the required buffer size in <b>TCHARs</b>, not including the terminating null character. On return of ERROR_SUCCESS, <i>pcchValueBuf</i> contains the number of <b>TCHARs</b> written to the buffer, not including the terminating null character. This parameter is an empty string if there are no errors.

### -param pcchValueBuf [in, out]

Pointer to the variable that specifies the size, in <b>TCHARs</b>, of the buffer pointed to by the variable <i>szValueBuf</i>. When the function returns ERROR_SUCCESS, this variable contains the size of the data copied to <i>szValueBuf</i>, not including the terminating null character. If <i>szValueBuf</i> is not large enough, the function returns ERROR_MORE_DATA and stores the required size, not including the terminating null character, in the variable pointed to by <i>pcchValueBuf</i>.

## -returns

The 
<b>MsiSummaryInfoGetProperty</b> function returns one of the following values:

## -remarks

If ERROR_MORE_DATA is returned, the parameter which is a pointer gives the size of the buffer required to hold the string. If ERROR_SUCCESS is returned, it gives the number of characters written to the string buffer. Therefore you can get the size of the buffer by passing in an empty string (for example "") for the parameter that specifies the buffer. Do not attempt to determine the size of the buffer by passing in a Null (value=0).

Windows Installer functions that return data in a user provided memory location should not be called with null as the value for the pointer. These functions return a string or return data as integer pointers, but return inconsistent values when passing null as the value for the output argument. For more information, see 
<a href="/windows/desktop/Msi/passing-null-as-the-argument-of-windows-installer-functions">Passing Null as the Argument of Windows Installer Functions</a>.

The property information returned by the <b>MsiSummaryInfoGetProperty</b> function is received by the <i>piValue</i>, <i>pftValue</i>, or  <i>szValueBuf</i> parameter depending upon the type of property value that has been specified in the <i>puiDataType</i> parameter.





> [!NOTE]
> The msiquery.h header defines MsiSummaryInfoGetProperty as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Msi/passing-null-as-the-argument-of-windows-installer-functions">Passing Null as the Argument of Windows Installer Functions</a>



<a href="/windows/desktop/Msi/database-functions">Summary Information Property Functions</a>



<a href="/windows/desktop/Msi/summary-information-stream-property-set">Summary Information Stream Property Set</a>



<a href="/windows/desktop/Msi/summaryinfo-summaryinfo">Summaryinfo.Property</a>
