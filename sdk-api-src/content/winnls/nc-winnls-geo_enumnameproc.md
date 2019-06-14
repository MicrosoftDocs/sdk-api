---
UID: NC:winnls.GEO_ENUMNAMEPROC
title: GEO_ENUMNAMEPROC (winnls.h)
author: windows-sdk-content
description: An application-defined callback function that processes enumerated geographical location information provided by the EnumSystemGeoNames function.
old-location: intl\geo_enumnameproc.htm
tech.root: Intl
ms.assetid: 51C64387-5BDF-463B-8A93-9748C099BB09
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Geo_EnumNameProc, Geo_EnumNameProc callback, Geo_EnumNameProc callback function [Internationalization for Windows Applications], intl.geo_enumnameproc, winnls/Geo_EnumNameProc
ms.topic: callback
req.header: winnls.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1709 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - UserDefined
api_location:
 - Winnls.h
api_name:
 - Geo_EnumNameProc
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GEO_ENUMNAMEPROC callback function


## -description


An application-defined callback function that processes enumerated geographical location information provided by the <a href="https://docs.microsoft.com/windows/desktop/api/winnls/nf-winnls-enumsystemgeonames">EnumSystemGeoNames</a> function. The <b>GEO_ENUMNAMEPROC</b> type defines a pointer to this callback function. <i>Geo_EnumNameProc</i> is a placeholder for the application-defined function name.


## -parameters




### -param Arg1


### -param Arg2








#### - GeoName [in]

A two-letter International Organization for Standardization (ISO) 3166-1 code or numeric United Nations (UN) Series M, Number 49  (M.49) code for a geographical location that is available on the operating system.


#### - data

Application-specific information that was specified by the data parameter when the application called the <a href="https://docs.microsoft.com/windows/desktop/api/winnls/nf-winnls-enumsystemgeonames">EnumSystemGeoNames</a> function.


## -returns



Returns <b>TRUE</b> to continue enumeration or <b>FALSE</b> otherwise.




## -remarks



An <i>Geo_EnumNameProc</i> function can carry out any desired task, and can use the information passed to it in the <i>data</i> parameter for any desired purpose. The application registers this function by passing its address to the <a href="https://docs.microsoft.com/windows/desktop/api/winnls/nf-winnls-enumsystemgeonames">EnumSystemGeoNames</a> function.

For information about two-letter ISO 3166-1 codes, see <a href="https://go.microsoft.com/fwlink/p/?linkid=859039">Country Codes - ISO 3166</a>.  For information about numeric UN M.49 codes, see <a href="https://go.microsoft.com/fwlink/p/?linkid=859018">Standard country or area codes for statistical use (M49)</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winnls/nf-winnls-enumsystemgeonames">EnumSystemGeoNames</a>



<a href="https://docs.microsoft.com/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="https://docs.microsoft.com/windows/desktop/Intl/national-language-support-functions">National Language Support Functions</a>
 

 

