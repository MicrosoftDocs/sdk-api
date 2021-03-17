---
UID: NF:vswriter.IVssComponentEx.GetPrepareForBackupFailureMsg
title: IVssComponentEx::GetPrepareForBackupFailureMsg (vswriter.h)
description: Returns the PrepareForBackup failure message string that a writer has set for a given component.
helpviewer_keywords: ["GetPrepareForBackupFailureMsg","GetPrepareForBackupFailureMsg method","GetPrepareForBackupFailureMsg method","IVssComponentEx interface","IVssComponentEx interface","GetPrepareForBackupFailureMsg method","IVssComponentEx.GetPrepareForBackupFailureMsg","IVssComponentEx::GetPrepareForBackupFailureMsg","base.ivsscomponentex_getprepareforbackupfailuremsg","vswriter/IVssComponentEx::GetPrepareForBackupFailureMsg"]
old-location: base\ivsscomponentex_getprepareforbackupfailuremsg.htm
tech.root: base
ms.assetid: b086ff8d-ff51-4550-887d-e7741e2469f2
ms.date: 12/05/2018
ms.keywords: GetPrepareForBackupFailureMsg, GetPrepareForBackupFailureMsg method, GetPrepareForBackupFailureMsg method,IVssComponentEx interface, IVssComponentEx interface,GetPrepareForBackupFailureMsg method, IVssComponentEx.GetPrepareForBackupFailureMsg, IVssComponentEx::GetPrepareForBackupFailureMsg, base.ivsscomponentex_getprepareforbackupfailuremsg, vswriter/IVssComponentEx::GetPrepareForBackupFailureMsg
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
req.lib: VssApi.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVssComponentEx::GetPrepareForBackupFailureMsg
 - vswriter/IVssComponentEx::GetPrepareForBackupFailureMsg
dev_langs:
 - c++
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
---

# IVssComponentEx::GetPrepareForBackupFailureMsg


## -description

Returns the <a href="/windows/desktop/VSS/vssgloss-p">PrepareForBackup</a> failure message string that a writer has set for a given component.

Both writers and requesters can call this method.

## -parameters

### -param pbstrFailureMsg [out]

A pointer to a null-terminated wide character string containing the failure message that describes an error that occurred 
      while processing a <a href="/windows/desktop/VSS/vssgloss-p">PrepareForBackup</a> 
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
No <a href="/windows/desktop/VSS/vssgloss-p">PrepareForBackup</a> failure message was set for the component.

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


```cpp
#include <windows.h>
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
    CComPtr<IVssWriterComponentsExt> spWriter;
    CComPtr<IVssComponent>   spComponent;
    CComPtr<IVssComponentEx> spComponentEx;
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

    CHK( pBackup->GetWriterComponentsCount( &cWriterComponents ) );

    for( iWriterComponent = 0; iWriterComponent < cWriterComponents; iWriterComponent++ )
    {
        spWriter.Release();
        CHK( pBackup->GetWriterComponents( iWriterComponent, &spWriter ) );
        CHK( spWriter->GetWriterInfo(&idInstance, &idWriter) );
        if( idWriter != c_ASRWriterId )
        {
            continue;
        }
        
        CHK( spWriter->GetComponentCount(&cComponents) );
        for( iComponent = 0; iComponent < cComponents; iComponent++ )
        {
            spComponent.Release();
            spComponentEx.Release();
            CHK( spWriter->GetComponent(iComponent, &spComponent) );
            CHK( spComponent->QueryInterface(__uuidof(IVssComponentEx), (void**)&spComponentEx) );

            bstrFailureMsg.Empty();
            CHK( spComponentEx->GetPrepareForBackupFailureMsg(&bstrFailureMsg) );

            if( ::SysStringLen(bstrFailureMsg) != 0 )
            {
                //  Write into the event log.
                Log_SPP_ERROR_WRITER( &ft, __LINE__, pwszWriterName, bstrFailureMsg );

                //  The ASR writer writes the same message to all components. 
                //  Log the message once.
                break;
            }
        }
    }

exit:
    return hr;
}


```

## -see-also

<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpreparebackup">CVssWriter::OnPrepareBackup</a>



<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsscomponentex">IVssComponentEx</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponentex-setprepareforbackupfailuremsg">IVssComponentEx::SetPrepareForBackupFailureMsg</a>