---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IMediaParams::AddEnvelope


## -description



The <code>AddEnvelope</code> method adds an envelope to a parameter.




## -parameters




### -param dwParamIndex [in]

Zero-based index of the parameter, or DWORD_ALLPARAMS to add the envelope to every parameter.


### -param cSegments




### -param pEnvelopeSegments






#### - cPoints [in]

Number of segments in the envelope.


#### - pEnvelope [in]

Pointer to an array of <a href="https://msdn.microsoft.com/b7386b63-c563-42dd-851c-780bf1043f65">MP_ENVELOPE_SEGMENT</a> structures that define the envelope segments. The size of the array is given in the <i>cPoints</i> parameter.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Index out of range.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMEORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
</table>
 




## -remarks



The caller should add envelopes in time-ascending order. Otherwise, the results on playback are indeterminate. If one envelope overlaps another, the later envelope takes precedence.

To enumerate the parameters supported by this object, along with their index values, use the <a href="https://msdn.microsoft.com/80c7da71-7898-4bda-a181-09ad8906532a">IMediaParamInfo</a> interface.


#### Examples

The following code sets two envelope segments, both using a linear function.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
#define MSEC 10000  // One millisecond

// Define an array with two segments. Note the segments appear in 
// time-ascending order.
MP_ENVELOPE_SEGMENT Segments[] =
{
    {  
        0,                  // rtStart
        3 * MSEC,           // rtStop
        0,                  // valStart
        12,                 // valStop
        MP_CURVE_LINEAR,    // iCurve
        MPF_ENVLP_STANDARD  // flags
    },
    {  
        6 * MSEC,
        9 * MSEC,
        12,
        0,
        MP_CURVE_LINEAR,
        MPF_ENVLP_STANDARD
    }
};
// Define the number of segments in the array.
DWORD cSegments = sizeof(Segments) / sizeof(Segments[0]);
DWORD dwParam = 0;  // Which parameter to set.

hr = pMediaParams-&gt;AddEnvelope(dwParam, cSegments, Segments);
</pre>
</td>
</tr>
</table></span></div>
This example assumes that the caller has previous used the <b>IMediaParamInfo</b> interface to query whether the DMO supports the MP_CURVE_LINEAR curve for that parameter.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/68ea8f6a-4b6d-4d79-a986-6032b767147b">IMediaParams Interface</a>
 

 

