---
UID: NF:bdaiface.IFrequencyMap.put_CountryCode
title: IFrequencyMap::put_CountryCode
author: windows-sdk-content
description: The put_CountryCode method sets the country/region code on the Network Provider filter.
old-location: mstv\ifrequencymap_put_countrycode.htm
old-project: mstv
ms.assetid: 8473e292-b47b-4c1a-b45e-b8acf0e36263
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IFrequencyMap interface [Microsoft TV Technologies],put_CountryCode method, IFrequencyMap.put_CountryCode, IFrequencyMap::put_CountryCode, IFrequencyMapput_CountryCode, bdaiface/IFrequencyMap::put_CountryCode, mstv.ifrequencymap_put_countrycode, put_CountryCode, put_CountryCode method [Microsoft TV Technologies], put_CountryCode method [Microsoft TV Technologies],IFrequencyMap interface
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: bdaiface.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: UICloseReasonType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdaiface.h
api_name:
 - IFrequencyMap.put_CountryCode
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IFrequencyMap::put_CountryCode


## -description



The <b>put_CountryCode</b> method sets the country/region code on the Network Provider filter.




## -parameters




### -param ulCountryCode [in]

Specifies the country/region code.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



If the method succeeds, the Network Provider loads the frequency table for the specified country/region code. It uses this table in all subsequent calls to <a href="https://msdn.microsoft.com/en-us/library/Dd694868(v=VS.85).aspx">IScanningTuner</a> methods.

If the country/region code does not match an existing frequency table, the method fails and the Network Provider continues to use the previous table. However, it stores the new country/region code, and the application can create a new frequency table by calling the <b>put_FrequencyMapping</b> method. This behavior enables an application to define new country/region codes with new frequency tables.

For a list of existing country/region codes, see <a href="https://msdn.microsoft.com/en-us/library/Dd387951(v=VS.85).aspx">Country/Region Assignments</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd375623(v=VS.85).aspx">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd694086(v=VS.85).aspx">IFrequencyMap Interface</a>
 

 

