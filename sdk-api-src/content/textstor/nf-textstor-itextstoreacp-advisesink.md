---
UID: NF:textstor.ITextStoreACP.AdviseSink
title: ITextStoreACP::AdviseSink
author: windows-sdk-content
description: The ITextStoreACP::AdviseSink method installs a new advise sink from the ITextStoreACPSink interface or modifies an existing advise sink. The sink interface is specified by the punk parameter.
old-location: tsf\itextstoreacp_advisesink.htm
old-project: TSF
ms.assetid: aadf54e4-25ba-4280-a184-e1d2a2594c3c
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: AdviseSink, AdviseSink method [Text Services Framework], AdviseSink method [Text Services Framework],ITextStoreACP interface, ITextStoreACP interface [Text Services Framework],AdviseSink method, ITextStoreACP.AdviseSink, ITextStoreACP::AdviseSink, _tsf_itextstoreacp_advisesink_ref, textstor/ITextStoreACP::AdviseSink, tsf.itextstoreacp_advisesink
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Textstor.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TsRunType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	msctf.dll
api_name:
-	ITextStoreACP.AdviseSink
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextStoreACP::AdviseSink


## -description


The <b>ITextStoreACP::AdviseSink</b> method installs a new advise sink from the <a href="https://msdn.microsoft.com/d7e5a04f-7159-436e-a522-4cb63063aeef">ITextStoreACPSink</a> interface or modifies an existing advise sink. The sink interface is specified by the <i>punk</i> parameter.


## -parameters




### -param riid [in]

Specifies the sink interface.


### -param punk [in]

Pointer to the sink interface. Cannot be <b>NULL</b>.


### -param dwMask [in]

Specifies the events that notify the advise sink. For more information about possible parameter values, see <a href="https://msdn.microsoft.com/8f406b67-f846-4712-b4be-811dbcc6ad55">TS_AS_* Constants</a>.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CONNECT_E_ADVISELIMIT</b></dt>
</dl>
</td>
<td width="60%">
A sink interface pointer could not be obtained.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The specified sink interface is unsupported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The specified sink object could not be obtained.

</td>
</tr>
</table>
 




## -remarks



Subsequent calls with the same interface, represented by the <i>punk</i> parameter, are handled as requests to update the <i>dwMask</i> parameter. Servers should not call the <b>AddRef</b> method on the sink in response to such a request.

Servers only maintain a single connection point. Attempts to advise a second sink object fail until the original sink object is removed. Applications should use the <a href="https://msdn.microsoft.com/11445652-e349-46a4-8887-1d1127e16275">ITextStoreACP::UnadviseSink</a> method to unregister the sink object when notifications are not required.

Use this method to get the <a href="https://msdn.microsoft.com/8c84429c-3f99-4ab1-b994-e4e93cd9c86d">ITextStoreACPServices</a> interface.


#### Examples

CMyTextEditor
          <a href="https://msdn.microsoft.com/21e011f7-6791-4eb9-85c9-18bd10107119">
            ITextStoreACP
          </a>


<div class="code"></div>
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
STDMETHODIMP CMyTextEditor::AdviseSink(REFIID riid, IUnknown *punk, DWORD dwMask)
{
        HRESULT         hr;
        IUnknown                *punkID;
        typedef struct
        {
        IUnknown                *punkID;
        ITextStoreACPSink       *pTextStoreACPSink;
        DWORD                   dwMask;
        }ADVISE_SINK, *PADVISE_SINK;    
        
        // Determine if the sink interface exists. 
        // Get the pointer to the IUnknown interface and check if the IUnknown 
        // pointer is the same as a pointer to an existing sink. 
        // If the sink exists, update the existing sink with the  
        // dwMask parameters passed to this method.      
        hr = QueryInterface(IID_IUnknown, (LPVOID*)&amp;punkID);

        if(FAILED(hr))
        {
                hr = E_INVALIDARG;
        }       

        if(punkID == m_AdviseSink.punkID)
        {
                m_AdviseSink.dwMask = dwMask;
                hr = S_OK;
        }

        // If the sink does not exist, do the following: 
        // 1. Install a new sink. 
        // 2. Keep the pointer to the IUnknown interface to uniquely 
        //        identify this advise sink. 
        // 3. Set the dwMask parameter of this new sink to the dwMask  
        //    parameters passed to this method. 
        // 4. Increment the reference count. 
        // 5. Release the IUnknown pointer, since this pointer is no 
        //        longer required. 

        if(IsEqualIID(riid, IID_ITextStoreACPSink))
        {
                punk-&gt;QueryInterface(IID_ITextStoreACPSink,
                         (LPVOID*)&amp;m_AdviseSink.pTextStoreACPSink);
                m_AdviseSink.punkID = punkID;
                m_AdviseSink.dwMask = dwMask;
                punkID-&gt;AddRef();
                punkID-&gt;Release();

                hr = S_OK;
        }
        return hr;
        
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/21e011f7-6791-4eb9-85c9-18bd10107119">
        ITextStoreACP
      </a>



<a href="https://msdn.microsoft.com/11445652-e349-46a4-8887-1d1127e16275">
        ITextStoreACP::UnadviseSink
      </a>



<a href="https://msdn.microsoft.com/8c84429c-3f99-4ab1-b994-e4e93cd9c86d">
        ITextStoreACPServices
      </a>



<a href="https://msdn.microsoft.com/8f406b67-f846-4712-b4be-811dbcc6ad55">TS_AS_* Constants
      </a>
 

 

