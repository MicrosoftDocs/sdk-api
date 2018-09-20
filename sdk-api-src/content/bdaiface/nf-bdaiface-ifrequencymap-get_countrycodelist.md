---
UID: NF:bdaiface.IFrequencyMap.get_CountryCodeList
title: IFrequencyMap::get_CountryCodeList
author: windows-sdk-content
description: The get_CountryCodeList method returns a list of all the country/region codes for which the Network Provider has a frequency table.
old-location: mstv\ifrequencymap_get_countrycodelist.htm
tech.root: MSTV
ms.assetid: cc9e2f2e-3187-446e-b1e6-ae32da4413b9
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IFrequencyMap interface [Microsoft TV Technologies],get_CountryCodeList method, IFrequencyMap.get_CountryCodeList, IFrequencyMap::get_CountryCodeList, IFrequencyMapget_CountryCodeList, bdaiface/IFrequencyMap::get_CountryCodeList, get_CountryCodeList, get_CountryCodeList method [Microsoft TV Technologies], get_CountryCodeList method [Microsoft TV Technologies],IFrequencyMap interface, mstv.ifrequencymap_get_countrycodelist
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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



For a list of country/region codes, see <a href="https://msdn.microsoft.com/a71784eb-e6b4-4dab-91fc-103c39dd1591">Country/Region Assignments</a>.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/0f7f1b2c-a191-45f5-a645-367e898b6ee2">IFrequencyMap Interface</a>
 

 

