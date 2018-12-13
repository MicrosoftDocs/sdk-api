---
UID: NF:bdaiface.IFrequencyMap.get_CountryCode
title: IFrequencyMap::get_CountryCode
author: windows-sdk-content
description: The get_CountryCode method returns the country/region code the Network Provider is currently using. The country/region code determines which frequency table the Network Provider loads.
old-location: mstv\ifrequencymap_get_countrycode.htm
tech.root: mstv
ms.assetid: 3f5e4109-e424-40be-9b3c-7eeef895e677
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFrequencyMap interface [Microsoft TV Technologies],get_CountryCode method, IFrequencyMap.get_CountryCode, IFrequencyMap::get_CountryCode, IFrequencyMapget_CountryCode, bdaiface/IFrequencyMap::get_CountryCode, get_CountryCode, get_CountryCode method [Microsoft TV Technologies], get_CountryCode method [Microsoft TV Technologies],IFrequencyMap interface, mstv.ifrequencymap_get_countrycode
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
 - IFrequencyMap.get_CountryCode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFrequencyMap::get_CountryCode


## -description



The <b>get_CountryCode</b> method returns the country/region code the Network Provider is currently using. The country/region code determines which frequency table the Network Provider loads.




## -parameters




### -param pulCountryCode [out]

Pointer to a variable that receives the country/region code.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



For a list of country/region codes, see <a href="https://msdn.microsoft.com/a71784eb-e6b4-4dab-91fc-103c39dd1591">Country/Region Assignments</a>.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd694086(v=VS.85).aspx">IFrequencyMap Interface</a>
 

 

