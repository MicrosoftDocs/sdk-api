---
UID: NN:msctf.ITfRange
title: ITfRange (msctf.h)
description: The ITfRange interface is used by text services and applications to reference and manipulate text within a given context. The interface ID is IID_ITfRange.
helpviewer_keywords: ["ITfRange","ITfRange interface [Text Services Framework]","ITfRange interface [Text Services Framework]","described","_tsf_itfrange_ref","msctf/ITfRange","tsf.itfrange"]
old-location: tsf\itfrange.htm
tech.root: TSF
ms.assetid: b8889f7d-3228-4ecc-8d24-c04234d3101e
ms.date: 12/05/2018
ms.keywords: ITfRange, ITfRange interface [Text Services Framework], ITfRange interface [Text Services Framework],described, _tsf_itfrange_ref, msctf/ITfRange, tsf.itfrange
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfRange
 - msctf/ITfRange
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfRange
---

# ITfRange interface


## -description

The <b>ITfRange</b> interface is used by text services and applications to reference and manipulate text within a given context. The interface ID is IID_ITfRange.

## -inheritance

The <b>ITfRange</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfRange</b> also has these types of members:

## -remarks

The TSF manager implements this interface. For more information about ranges, anchors, embedded objects, and other text properties used by TSF, see <a href="/windows/desktop/TSF/ranges">Ranges</a>, <a href="/windows/desktop/TSF/embedded-objects">Embedded Objects</a>, and other topics within <a href="/windows/desktop/TSF/using-text-services-framework">Using Text Services Framework</a>.


#### Examples

Once an <a href="/windows/desktop/api/msctf/nn-msctf-itfcomposition">ITfComposition</a> composition object is instantiated, a pointer to an <b>ITfRange</b> interface pointer can be obtained by calling the <a href="/windows/desktop/api/msctf/nf-msctf-itfcomposition-getrange">ITfComposition::GetRange</a> method, as shown in the following code example.

<div class="code"></div>

```cpp

HRESULT         hr;
ITfComposition  *pComposition;
ITfRange        *pRange;
WCHAR           *achBuffer[64];  // Buffer to receive text. 
ULONG           cch;

hr = pComposition->GetRange(&pRange);
if(SUCCEEDED(hr))
{
    // Loop to scan text: 

    do
    {
        cch = ARRAYSIZE(achBuffer);
        hr = pRange->GetText(ec, TF_TF_MOVESTART | TF_TF_IGNOREEND, achBuffer, cch, &cch);
        if(SUCCEEDED(hr))
        {
            // Do something with the text. 

            pRange->Release();
        }
    }
    while (cch == ARRAYSIZE(achBuffer));

    pComposition->Release();
}

```


A pointer to a current <b>ITfRange</b> object can be obtained from the &lt;range&gt; element of the <a href="/windows/desktop/api/msctf/ns-msctf-tf_selection">TF_SELECTION</a> structure.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/TSF/compositions">Compositions</a>



<a href="/windows/desktop/TSF/embedded-objects">Embedded Objects</a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfcomposition">ITfComposition
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfcomposition-getrange">ITfComposition::GetRange
      </a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="/windows/desktop/TSF/ranges">Ranges</a>



<a href="/windows/desktop/api/msctf/ns-msctf-tf_selection">TF_SELECTION
      </a>



<a href="/windows/desktop/TSF/using-text-services-framework">Using Text Services Framework</a>
