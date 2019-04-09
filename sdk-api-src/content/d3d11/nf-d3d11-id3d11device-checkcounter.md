---
UID: NF:d3d11.ID3D11Device.CheckCounter
title: ID3D11Device::CheckCounter (d3d11.h)
author: windows-sdk-content
description: Get the type, name, units of measure, and a description of an existing counter.
old-location: direct3d11\id3d11device_checkcounter.htm
tech.root: direct3d11
ms.assetid: b09feac6-79c8-4f40-bfa1-028d4490b039
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 6fe48914-c164-b2f3-ada5-6ebc529a69a9, CheckCounter, CheckCounter method [Direct3D 11], CheckCounter method [Direct3D 11],ID3D11Device interface, ID3D11Device interface [Direct3D 11],CheckCounter method, ID3D11Device.CheckCounter, ID3D11Device::CheckCounter, d3d11/ID3D11Device::CheckCounter, direct3d11.id3d11device_checkcounter
ms.topic: method
req.header: d3d11.h
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
req.lib: D3D11.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11Device.CheckCounter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11Device::CheckCounter


## -description


Get the type, name, units of measure, and a description of an existing counter.


## -parameters




### -param pDesc [in]

Type: <b>const <a href="https://msdn.microsoft.com/a0816409-fbe1-4b45-9b69-6f85b20008cb">D3D11_COUNTER_DESC</a>*</b>

Pointer to a counter description (see <a href="https://msdn.microsoft.com/a0816409-fbe1-4b45-9b69-6f85b20008cb">D3D11_COUNTER_DESC</a>). Specifies which counter information is to be retrieved about.
          


### -param pType [out]

Type: <b><a href="https://msdn.microsoft.com/c39ecf5c-f4c5-4caf-bcd6-2f1ea924ec64">D3D11_COUNTER_TYPE</a>*</b>

Pointer to the data type of a counter (see <a href="https://msdn.microsoft.com/c39ecf5c-f4c5-4caf-bcd6-2f1ea924ec64">D3D11_COUNTER_TYPE</a>). Specifies the data type of the counter being retrieved.
          


### -param pActiveCounters [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a>*</b>

Pointer to the number of hardware counters that are needed for this counter type to be created. All instances of the same counter type use the same hardware counters.


### -param szName [out, optional]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPSTR</a></b>

String to be filled with a brief name for the counter. May be <b>NULL</b> if the application is not interested in the name of the counter.
          


### -param pNameLength [in, out, optional]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a>*</b>

Length of the string returned to szName. Can be <b>NULL</b>.
          


### -param szUnits [out, optional]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPSTR</a></b>

Name of the units a counter measures, provided the memory the pointer points to has enough room to hold the string. Can be <b>NULL</b>. The returned string will always be in English.
          


### -param pUnitsLength [in, out, optional]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a>*</b>

Length of the string returned to szUnits. Can be <b>NULL</b>.
          


### -param szDescription [out, optional]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPSTR</a></b>

A description of the counter, provided the memory the pointer points to has enough room to hold the string. Can be <b>NULL</b>. The returned string will always be in English.
          


### -param pDescriptionLength [in, out, optional]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a>*</b>

Length of the string returned to szDescription. Can be <b>NULL</b>.
          


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a>.
          




## -remarks



Length parameters can be <b>NULL</b>, which indicates the application is not interested in the length nor the corresponding string value. When a length parameter is non-<b>NULL</b> and the corresponding string is <b>NULL</b>, the input value of the length parameter is ignored, and the length of the corresponding string (including terminating <b>NULL</b>) will be returned through the length parameter. When length and the corresponding parameter are both non-<b>NULL</b>, the input value of length is checked to ensure there is enough room, and then the length of the string (including terminating <b>NULL</b> character) is passed out through the length parameter.
        

<b>Windows Phone 8:
        </b> This API is supported.
      




## -see-also




<a href="https://msdn.microsoft.com/2f2559d9-1cd6-44f6-90e2-ee0f86e39f78">ID3D11Device</a>
 

 

