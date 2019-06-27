---
UID: NF:bdaiface.IFrequencyMap.get_CountryCodeList
title: IFrequencyMap::get_CountryCodeList (bdaiface.h)
author: windows-sdk-content
description: The get_CountryCodeList method returns a list of all the country/region codes for which the Network Provider has a frequency table.
old-location: mstv\ifrequencymap_get_countrycodelist.htm
tech.root: mstv
ms.assetid: cc9e2f2e-3187-446e-b1e6-ae32da4413b9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFrequencyMap interface [Microsoft TV Technologies],get_CountryCodeList method, IFrequencyMap.get_CountryCodeList, IFrequencyMap::get_CountryCodeList, IFrequencyMapget_CountryCodeList, bdaiface/IFrequencyMap::get_CountryCodeList, get_CountryCodeList, get_CountryCodeList method [Microsoft TV Technologies], get_CountryCodeList method [Microsoft TV Technologies],IFrequencyMap interface, mstv.ifrequencymap_get_countrycodelist
ms.topic: method
f1_keywords: 
 - "bdaiface/IFrequencyMap.get_CountryCodeList"
req.header: bdaiface.h
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
 - COM
api_location:
 - bdaiface.h
api_name:
 - IFrequencyMap.get_CountryCodeList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFrequencyMap::get_CountryCodeList


## -description



The <b>get_CountryCodeList</b> method returns a list of all the country/region codes for which the Network Provider has a frequency table.




## -parameters




### -param pulCount [out]

Pointer to a variable that receives the number of country/region codes.


### -param ppulList [out]

Pointer to a variable that receives the address of an array of size <i>pulCount</i>, allocated by the method. The array contains a list of the country/region codes. The caller must free the array by calling <b>CoTaskMemFree</b>.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



For a list of country/region codes, see <a href="https://docs.microsoft.com/windows/desktop/DirectShow/country-region-assignments">Country/Region Assignments</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nn-bdaiface-ifrequencymap">IFrequencyMap Interface</a>
 

 

