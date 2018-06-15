---
UID: NF:vswriter.IVssComponentEx.GetPrepareForBackupFailureMsg
title: IVssComponentEx::GetPrepareForBackupFailureMsg
author: windows-sdk-content
description: Returns the PrepareForBackup failure message string that a writer has set for a given component.
old-location: base\ivsscomponentex_getprepareforbackupfailuremsg.htm
old-project: VSS
ms.assetid: b086ff8d-ff51-4550-887d-e7741e2469f2
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: GetPrepareForBackupFailureMsg, GetPrepareForBackupFailureMsg method, GetPrepareForBackupFailureMsg method,IVssComponentEx interface, IVssComponentEx interface,GetPrepareForBackupFailureMsg method, IVssComponentEx.GetPrepareForBackupFailureMsg, IVssComponentEx::GetPrepareForBackupFailureMsg, base.ivsscomponentex_getprepareforbackupfailuremsg, vswriter/IVssComponentEx::GetPrepareForBackupFailureMsg
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: vswriter.h
req.include-header: Vss.h, VsWriter.h
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
tech.root: 
req.typenames: VSS_WRITERRESTORE_ENUM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VssApi.lib
 - VssApi.dll
api_name:
 - IVssComponentEx.GetPrepareForBackupFailureMsg
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVssComponentEx::GetPrepareForBackupFailureMsg


## -description


Returns the <a href="https://docs.microsoft.com/windows/desktop//VSS/vssgloss-p">PrepareForBackup</a> failure message string that a writer has set for a given component.

Both writers and requesters can call this method.


## -parameters




### -param pbstrFailureMsg [out]

A pointer to a null-terminated wide character string containing the failure message that describes an error that occurred 
      while processing a <a href="https://docs.microsoft.com/windows/desktop//VSS/vssgloss-p">PrepareForBackup</a> 
      event.


## -returns



The following are the valid return codes for this method.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The failure message was successfully obtained.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
No <a href="https://docs.microsoft.com/windows/desktop//VSS/vssgloss-p">PrepareForBackup</a> failure message was set for the component.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the parameter values is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The caller is out of memory or other system resources.

</td>
</tr>
</table>
 




## -remarks



The caller is responsible for freeing the string that  the <i>pbstrFailureMsg</i> parameter points to by calling the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include &lt;windows.h&gt;
#include "vss.h"
#include "vsmgmt.h"

#define CHKARG_ASSERT(EXPR)  
do
{
    if(! ( EXPR ) )               
    {                       
        assert(FALSE);      
        hr = E_INVALIDARG;  
        goto exit;          
    }                        
}
while ( FALSE, FALSE );

#define  CHK(HR)                
do
{
    hr =  ( HR ) ;                
    if(FAILED(HR))          
    {                       
        hr = HR;            
        goto exit;          
    }                       
}
while ( FALSE, FALSE ); 

STDMETHODIMP CheckAsrBackupErrorMsg
(
      IVssBackupComponents           *pBackup,
      const WCHAR              *pwszWriterName
)
{
    CComPtr&lt;IVssWriterComponentsExt&gt; spWriter;
    CComPtr&lt;IVssComponent&gt;   spComponent;
    CComPtr&lt;IVssComponentEx&gt; spComponentEx;
    UINT    cWriterComponents = 0;
    UINT    iWriterComponent = 0;
    UINT    cComponents = 0;
    UINT    iComponent = 0;
    VSS_ID  idWriter;
    VSS_ID  idInstance;
    CComBSTR bstrFailureMsg;
    HRESULT  hr = S_OK;
    CHKARG_ASSERT( pBackup );
    CHKARG_ASSERT( pwszWriterName );

    CHK( pBackup-&gt;GetWriterComponentsCount( &amp;cWriterComponents ) );

    for( iWriterComponent = 0; iWriterComponent &lt; cWriterComponents; iWriterComponent++ )
    {
        spWriter.Release();
        CHK( pBackup-&gt;GetWriterComponents( iWriterComponent, &amp;spWriter ) );
        CHK( spWriter-&gt;GetWriterInfo(&amp;idInstance, &amp;idWriter) );
        if( idWriter != c_ASRWriterId )
        {
            continue;
        }
        
        CHK( spWriter-&gt;GetComponentCount(&amp;cComponents) );
        for( iComponent = 0; iComponent &lt; cComponents; iComponent++ )
        {
            spComponent.Release();
            spComponentEx.Release();
            CHK( spWriter-&gt;GetComponent(iComponent, &amp;spComponent) );
            CHK( spComponent-&gt;QueryInterface(__uuidof(IVssComponentEx), (void**)&amp;spComponentEx) );

            bstrFailureMsg.Empty();
            CHK( spComponentEx-&gt;GetPrepareForBackupFailureMsg(&amp;bstrFailureMsg) );

            if( ::SysStringLen(bstrFailureMsg) != 0 )
            {
                //  Write into the event log.
                Log_SPP_ERROR_WRITER( &amp;ft, __LINE__, pwszWriterName, bstrFailureMsg );

                //  The ASR writer writes the same message to all components. 
                //  Log the message once.
                break;
            }
        }
    }

exit:
    return hr;
}

</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/4e88d92b-48f3-42f9-bf66-61337a745902">CVssWriter::OnPrepareBackup</a>



<a href="https://msdn.microsoft.com/b11f65b0-2de2-478b-88b6-4696a8da2419">IVssComponentEx</a>



<a href="https://msdn.microsoft.com/b2c48c06-8bfc-431b-aab3-89ec9b30a9a0">IVssComponentEx::SetPrepareForBackupFailureMsg</a>
 

 

