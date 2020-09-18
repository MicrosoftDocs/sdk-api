---
UID: NF:wmcontainer.IMFASFSplitter.GetSelectedStreams
title: IMFASFSplitter::GetSelectedStreams (wmcontainer.h)
description: Gets a list of currently selected streams.
helpviewer_keywords: ["GetSelectedStreams","GetSelectedStreams method [Media Foundation]","GetSelectedStreams method [Media Foundation]","IMFASFSplitter interface","IMFASFSplitter interface [Media Foundation]","GetSelectedStreams method","IMFASFSplitter.GetSelectedStreams","IMFASFSplitter::GetSelectedStreams","f2c12e45-f320-43e0-abf1-36993dfed32d","mf.imfasfsplitter_getselectedstreams","wmcontainer/IMFASFSplitter::GetSelectedStreams"]
old-location: mf\imfasfsplitter_getselectedstreams.htm
tech.root: mf
ms.assetid: f2c12e45-f320-43e0-abf1-36993dfed32d
ms.date: 12/05/2018
ms.keywords: GetSelectedStreams, GetSelectedStreams method [Media Foundation], GetSelectedStreams method [Media Foundation],IMFASFSplitter interface, IMFASFSplitter interface [Media Foundation],GetSelectedStreams method, IMFASFSplitter.GetSelectedStreams, IMFASFSplitter::GetSelectedStreams, f2c12e45-f320-43e0-abf1-36993dfed32d, mf.imfasfsplitter_getselectedstreams, wmcontainer/IMFASFSplitter::GetSelectedStreams
req.header: wmcontainer.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFASFSplitter::GetSelectedStreams
 - wmcontainer/IMFASFSplitter::GetSelectedStreams
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFASFSplitter.GetSelectedStreams
---

# IMFASFSplitter::GetSelectedStreams


## -description

Gets a list of currently selected streams.

## -parameters

### -param pwStreamNumbers [out]

The address of an array of <b>WORDs</b>. This array receives the stream numbers of the selected streams.
          This parameter can be <b>NULL</b>.

### -param pwNumStreams [in, out]

On input, points to a variable that contains the number of elements in the <i>pwStreamNumbers</i> array. Set the variable to zero if <i>pwStreamNumbers</i> is <b>NULL</b>. 

On output, receives the number of elements that were copied into <i>pwStreamNumbers</i>. Each element is the identifier of a selected stream.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_BUFFERTOOSMALL</b></dt>
</dl>
</td>
<td width="60%">
The <i>pwStreamNumbers</i> array is smaller than the number of selected streams.
              See Remarks.

</td>
</tr>
</table>

## -remarks

To get the number of selected streams, set <i>pwStreamNumbers</i> to <b>NULL</b>. The method will return <b>MF_E_BUFFERTOSMALL</b> but will also set the value of <code>*pwNumStreams</code> equal  to the number of selected streams. Then allocate an array of that size and call the method again, passing the array in the <i>pwStreamNumbers</i> parameter.

The following code shows these steps:


```cpp
HRESULT DisplaySelectedStreams(IMFASFSplitter *pSplitter)
{
    WORD count = 0;
    HRESULT hr = pSplitter->GetSelectedStreams(NULL, &count);
    if (hr == MF_E_BUFFERTOOSMALL)
    {
        WORD *pStreamIds = new (std::nothrow) WORD[count];
        if (pStreamIds)
        {
            hr = pSplitter->GetSelectedStreams(pStreamIds, &count);
            if (SUCCEEDED(hr))
            {
                for (WORD i = 0; i < count; i++)
                {
                    printf("Selected stream ID: %d\n", pStreamIds[i]);
                }
            }
            delete [] pStreamIds;
        }
        else
        {
            hr = E_OUTOFMEMORY;
        }
    }
    return hr;
}

```


Alternatively, you can allocate an array that is equal to the total number of streams and pass that to <i>pwStreamNumbers</i>.

Before calling this method, initialize <code>*pwNumStreams</code>  to the number of elements in <i>pwStreamNumbers</i>. If <i>pwStreamNumbers</i> is <b>NULL</b>, set <code>*pwNumStreams</code> to zero.

By default, no streams are selected by the splitter. Select streams by calling the <a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-selectstreams">IMFASFSplitter::SelectStreams</a> method.

## -see-also

<a href="/windows/desktop/medfound/asf-splitter">ASF Splitter</a>



<a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter">IMFASFSplitter</a>