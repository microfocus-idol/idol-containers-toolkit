ARG IDOL_VERSION
ARG REGISTRY

FROM ${REGISTRY}/content:${IDOL_VERSION}

ARG CONTENT_CFG=content.cfg
ARG SECURITYINFOKEYS
ARG DOCUMENT_SECURITY_TYPE=NT_V4
ARG DOCUMENT_SECURITY_TYPE_MODE=AUTONOMY_SECURITY_V4_NT_MAPPED
ARG DOCUMENT_SECURITY_TYPE_PROPMATCH=nt_v4

COPY $CONTENT_CFG /content/cfg/content.cfg

RUN sed -i "s/XX_SECURITYINFOKEYS_XX/${SECURITYINFOKEYS}/g" /content/cfg/content.cfg \
    && sed -i "s/XX_DOCUMENT_SECURITY_TYPE_XX/${DOCUMENT_SECURITY_TYPE}/g" /content/cfg/content.cfg \
    && sed -i "s/XX_DOCUMENT_SECURITY_TYPE_MODE_XX/${DOCUMENT_SECURITY_TYPE_MODE}/g" /content/cfg/content.cfg \
    && sed -i "s/XX_DOCUMENT_SECURITY_TYPE_PROPMATCH_XX/${DOCUMENT_SECURITY_TYPE_PROPMATCH}/g" /content/cfg/content.cfg
